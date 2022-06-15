## Faster-Rcnn：随机初始化的Faster R-CNN
---

## 目录
1. [所需环境](#所需环境)
2. [文件下载](#文件下载)
3. [训练步骤](#训练步骤)
4. [训练结果和Tensorboard可视化](#训练结果和tensorboard可视化)
 

## 所需环境
linux操作系统，torch == 1.2.0

## 文件下载
VOC07+12数据集下载地址如下：  
链接: https://pan.baidu.com/s/1fXg-h0YDihGqxSg_td_Zng?pwd=j7qk
提取码：j7qk

## 训练步骤
1. 数据集的准备   
**使用VOC格式进行训练，训练前需要下载好VOC07+12的数据集，解压后放在根目录**  

2. 数据集的处理   
运行voc_annotation.py生成根目录下的2007_train.txt和2007_val.txt。   

3. 开始训练   
train.py用于训练VOC数据集，可以调整batchsize，learning rate，epoch等参数。设置完成后直接运行train.py即可开始训练。   


## 训练结果和Tensorboard可视化
1. 训练后会在logs/loss_xx文件夹下生成events.out.tfevents.xxx文件，同时logs文件夹下会生成最佳权值.pth文件。

2. 进入到logs/loss_xx文件夹下后输入tensorboard --logdir='events.out.tfevents.xxx的保存路径' --port=6006

3. 运行以上命令后打开生成的网址即可查看利用Tensorboard可视化后的train loss，val loss以及mAP曲线。

