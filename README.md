# API_ML_AI
## PRD

### Product Requirements
| | |
|--------------|----|
|Target release|2018/11/26|
|epic|购车&修车指南|
|Document Status|进行中|
|Document owner|叶家杰|
|Designer|叶家杰|
|Developer|叶家杰|

### Goals
在懂车帝APP增添为用户提供能够显示用户所在地附近4S店和汽车修理厂的位置的功能。
### Background and strategic fit：
1. 背景：
- 自身：1、懂车帝APP产品定位是汽车垂直媒体，为用户提供的看车、选车、买车方面的服务模块。但是，APP里并没有为用户提供当地汽车4s店的具体位置。目前为止，大部分人购车都是通过到实体门店试车后才会下决定的。2、APP里有提供道路救援的功能，目前只有“拖车救援”“路修救援”的收费服务，用户处于被动收费的局面。3、APP里“拍照识车”功能存在延时性
- 整体：在市面上，在汽车类资讯APP中，最主要的功能应该就是资讯信息列表、论坛和汽车产品库，对于提供上述两个功能的应用基本没有。
2. 战略契合处：
- 可以在看车、选车、买车这个服务模块基础上添加一个能够根据用户所在位置提供当地实体店位置的功能。
- 可以完善APP里“道路救援”的功能，为用户提供距离最近多家汽车修配厂、汽车4s门店的位置及联系方式，让用户主动联系这些厂家，掌握主动权。
- 懂车帝如果能够推行上述两个功能，在市场竞争方面能偶更胜一筹。
- 完善APP拍照识车功能，提高时效性。
### Assumptions: 
- 为准备购置新车但对当地汽车门店不熟悉的用户适用。
- 为在行车过程中车子突然发生故障或发现车子存在隐患的用户适用。
- 用户在使用此功能时，要先懂得使用“拍照识车”功能的。
- 用户在使用过程必须打开GPS定位，以便获得精准的位置定位。
- 必须在懂车帝APP里使用。
### Requirements：

|#|title|User story|importance|Notes |
|--------------|----|----|-----|-----|
|1|我该去哪里看车啊|当我在懂车帝APP上看中了一台奥迪A3新能源插电式混合动力汽车，我想了解广州从化的门店是否有这辆车在售，但是我却不知道这些门店的具体位置，也不知道该怎么到这些门店去，我该怎么办？这时候能够通过使用【实体店看车】功能便能够解决这个具体问题。|主要功能|4s门店位置|
|2|我想叫附近最近的汽车修配厂的拖车服务|我在回中山大学南方学院的过程中，车子发生故障被迫停在路边上。我并不知道附近最近的汽车修配厂的服务电话，又不想在应用上叫拖车服务，我想叫最近的汽车修配厂的推车服务啊，怎么办？这时候可以通过【联系汽修厂】的功能得到最近的汽修厂联系电话，于是我叫来了这家店的拖车服务。|次要功能|用户位置、汽修厂|
|3|我想知道这辆车的型号|我今天在学校路上看到一辆很炫的车，我想知道这是什么车型，于是我打开应用里的【拍照识车】功能，了解到这是一款奥迪A3新能源插电式混合动力汽车。|次要功能|拍照识车|

### User interaction and design
- 1.所需添加的功能（“✔”）
![目前APP上的主要功能](https://github.com/Yejiejie/API_ML_AI/blob/master/%E7%9B%AE%E5%89%8DAPP%E4%B8%8A%E4%B8%BB%E8%A6%81%E5%8A%9F%E8%83%BD%26%E8%A6%81%E5%A2%9E%E5%8A%A0%E5%8A%9F%E8%83%BD.png)
- 2.流程图
![推荐路线流程图](https://github.com/Yejiejie/API_ML_AI/blob/master/%E7%94%A8%E6%88%B7%E6%B5%81%E7%A8%8B%E5%9B%BE.png)
- 3.产品原型图（待完善）
![产品原型图1](https://github.com/Yejiejie/API_ML_AI/blob/master/%E5%8E%9F%E5%9E%8B1.png)
![产品原型图2](https://github.com/Yejiejie/API_ML_AI/blob/master/%E5%8E%9F%E5%9E%8B2.png)
### Questions:
|Question|Outcome|
|--------|-------|
|如何实现输出4S店门面与地图联系相一致|待完善|
|百度地图如何显示用户所在位置|待完善|
|如何实现类似车型精准反馈|待完善|
|如何提高拍照识车的时效性|待完善|
### Not doing: 
路线推荐系统
### API&AI
- 百度地图API
- 细粒度图像识别（车型识别、品牌logo识别）
[链接](http://ai.baidu.com/tech/imagerecognition/fine_grained)
### Nurture plan
### 加值宣言
通过调用百度地图API，将用户所位置标示出来，并且显示用户附近汽车4S店的位置，能够让用户获知到4S店具体方位。除此之外还提供附近汽车修理厂的位置的功能。
### 核心价值
为懂车帝APP增加定位功能
### 用户痛点
- 用户在懂车帝APP上获取了某款车的资讯，但是APP没有提供当地门店的具体位置的功能，难以到门店去看车试车。
- APP上提供的【4S店保养】功能并没有提供所推荐的4S店的具体位置，还要手动搜索。
### 人工智能概率性与用户痛点
### 需求列表与人工智能API加值
### 原型
### API调配输入输出
- [Key1](http://lbsyun.baidu.com/apiconsole/key)
- [key2](https://console.bce.baidu.com/ai/?_=1544405088209&fromai=1#/ai/imagerecognition/overview/index)
- [技术文档](http://lbsyun.baidu.com/index.php?title=androidsdk)
### 效果（理想）
![API调用](https://github.com/Yejiejie/API_ML_AI/blob/master/API%E8%B0%83%E7%94%A8.png)
![logo识别输入](https://github.com/Yejiejie/API_ML_AI/blob/master/logo%E8%AF%86%E5%88%AB%E8%BE%93%E5%85%A5.png)
![logo识别输出](https://github.com/Yejiejie/API_ML_AI/blob/master/logo%E8%AF%86%E5%88%AB%E8%BE%93%E5%87%BA.png)
![车型识别输入](https://github.com/Yejiejie/API_ML_AI/blob/master/%E8%BD%A6%E5%9E%8B%E8%AF%86%E5%88%AB%E8%BE%93%E5%85%A5.png)
![车型识别输出](https://github.com/Yejiejie/API_ML_AI/blob/master/%E8%BD%A6%E5%9E%8B%E8%AF%86%E5%88%AB%E8%BE%93%E5%87%BA.png)
### 现实调用（待放上）
(```)
from bs4 import Car
from urllib import request
from aip import AipImageClassify​AipSpeech
import IPython
APP_ID = '15106563'
API_KEY = '3yZGOA0MF7vIaVSkU5tSuqH5
SECRET_KEY = 'QsGBB6PLUkBGOl8tYAGfEsKFqOwpnwhB'
client = AipSpeech(APP_ID, API_KEY, SECRET_KEY)
def get_file_content(filePath):
    with open(filePath, 'rb') as fp:
        return fp.read()

image = get_file_content('example.jpg')
client.logoSearch(image);

options = {}
options["custom_lib"] = "true"


client.logoSearch(image, options

