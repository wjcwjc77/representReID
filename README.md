# representReID
## train.py 是训练的代码，请在anaconda prompt中cd到train.py的当前目录，然后输入 python train.py 开始训练
## util文件夹：
#### utils.py: 是一些工具，可忽略
#### transforms.py: 做数据增广，将图片放大，然后随机crop出给定高宽的大小
#### optimizers.py: 封装一下pytorch的优化器
#### losses.py: 封装一些损失函数，在表征学习中，我们只计算id损失，即交叉熵损失函数
#### data_manager.py: 读取所有的数据集（train, query, gallery）,并对数据集进行处理（读取每一张图片名，然后提取出id，cmid，连上完整的图片路径返回）
#### data_loader.py: 继承pytorch的Dataset类，然后定义三个函数（__init__,__len__,__getitem__）
<img width="718" alt="image" src="https://github.com/wjcwjc77/representReID/assets/115401950/50cf6d9f-d3c1-4c97-8ec7-e67a40c17448">

## models文件夹：
#### 一些网络（导入预训练，对网络部分重构）
本项目中使用resnet50

## 数据集文件夹
新键data文件夹，然后下载market1501数据集放在data文件夹下（下载地址：https://drive.google.com/file/d/0B8-rUzbwVRk0c054eEozWG9COHM/view?resourcekey=0-8nyl7K9_x37HlQm34MmrYQ）
![image](https://github.com/wjcwjc77/representReID/assets/115401950/1c6d5ae7-d17c-41d9-8898-1cc4b55dd805)



