# API_ML_AI
## PRD

### Product Requirements
|Target release|2018/11/26|
|--------------|----|
|epic|为懂车帝APP添加可行性功能|
|Document Status|进行中|
|Document owner|叶家杰|
|Designer|叶家杰|
|Developer|叶家杰|


### PRD：
#### 1. 背景（用户痛点）：
##### 自身：
- 1.经过调查，到目前为止，大部分人购车都是通过到实体门店试车后才会下决定的。懂车帝APP产品定位是汽车垂直媒体，为用户提供的看车、选车、买车方面的服务。但是APP并没有提供当地门店的具体位置的功能，用户虽然在懂车帝APP上获取了某款车的资讯，但是对于获得具体的4S门店位置信息还需手动搜索。
- 2.懂车帝APP里的拍照识车功能存在延时性，只属于娱乐功能（根据人脸判断匹配车辆），并不能满足用户通过拍照或者图片得到反馈车辆品牌、型号的需求。

##### 整体：在市面上，在汽车类资讯APP中，最主要的功能应该就是资讯信息列表、论坛和汽车产品库，对于提供上述两个功能的应用尚未开发。

#### 2. 战略契合处（加值宣言）：
- 1.可以在看车、选车、买车这个服务模块基础上添加通过调用地图API，将用户所位置标示出来，并且显示用户附近汽车4S店的位置，能够让用户获知到4S店具体位置。
- 2.完善APP拍照识车功能，提高时效性。
- 3.懂车帝如果能够推行上述两个功能，在市场竞争方面能偶更胜一筹。

#### 3.产品概述
- 核心功能（核心价值）：为懂车帝APP增加地图搜索功能。
- 延伸功能：为懂车帝APP增加图像识别（车型识别）功能。
#### Goals（产品目标）
在懂车帝APP增添为用户提供能够显示用户所在地附近4S店的位置的功能和用户能够通过拍照或者图像来获得该车型信息的功能。

#### Assumptions产品使用场景设想（人工智能概率性与用户痛点)：

|#|场景|方式|可行性概率|
|-|---|----|----------|
|1|日常生活中|检测用户上传的车辆图片，识别所属车型，包括车辆品牌及具体型号、颜色、年份、位置信息。|＞95%|
|2|日常生活中|检测图片中出现的所有车辆，返回车辆类型与位置。|＞80%|
|3|日常生活中|通过GPS定位，基站定位，混合定位三种定位模式为用户提供高精度的定位服务|＞95%|

#### Requirements（需求列表与人工智能API加值）:

|#|title|User story|importance|API|
|--------------|----|----|-----|-----|
|1|我该去哪里看车啊|当我在懂车帝APP上看中了一台奥迪A3新能源插电式混合动力汽车，我想了解广州从化的门店是否有这辆车在售，但是我却不知道这些门店的具体位置，也不知道该怎么到这些门店去，我该怎么办？这时候能够通过使用【实体店看车】功能便能够解决这个具体问题。|可行性≥95%|定位|
|2|我想知道这辆车的型号|我今天在学校路上看到一辆很炫的车，我想知道这是什么车型，于是我打开应用里的【拍照识车】功能，了解到这是一款奥迪A3新能源插电式混合动力汽车。|可行性≥90%|车型识别|

#### Not doing: 
路线推荐系统

### 原型：

#### User interaction and design
##### 1.所需添加的功能（“✔”）
![目前APP上主要功能要增加功能](https://github.com/Yejiejie/API_ML_AI/blob/master/%E7%9B%AE%E5%89%8DAPP%E4%B8%8A%E4%B8%BB%E8%A6%81%E5%8A%9F%E8%83%BD%E8%A6%81%E5%A2%9E%E5%8A%A0%E5%8A%9F%E8%83%BD.png)
##### 2.用户流程图
- 功能一【实体店看车】![功能一：【实体店看车】功能流程图.](https://github.com/Yejiejie/API_ML_AI/blob/master/%E5%8A%9F%E8%83%BD%E4%B8%80%EF%BC%9A%E3%80%90%E5%AE%9E%E4%BD%93%E5%BA%97%E7%9C%8B%E8%BD%A6%E3%80%91%E5%8A%9F%E8%83%BD%E6%B5%81%E7%A8%8B%E5%9B%BE.png)

- 功能二：【拍照识图】![功能二：【拍照识图】用户流程图](https://github.com/Yejiejie/API_ML_AI/blob/master/%E5%8A%9F%E8%83%BD%E4%BA%8C%EF%BC%9A%E3%80%90%E6%8B%8D%E7%85%A7%E8%AF%86%E5%9B%BE%E3%80%91%E7%94%A8%E6%88%B7%E6%B5%81%E7%A8%8B%E5%9B%BE.png)
##### 3.产品原型图（待完善）
[原型文档](https://yejiejie.github.io/yuanxing/)

### API&AI

#### 需要用到的API
- 百度地图API、高德地图API
- 细粒度图像识别（车型识别、品牌logo识别）
[链接](http://ai.baidu.com/tech/imagerecognition/fine_grained)

#### API调配输入输出
##### 1.地图搜索功能
###### 理想效果
###### 现实调用
###### 试用报告分析&风险分析
##### 2.车型识别
- [技术文档](http://lbsyun.baidu.com/index.php?title=androidsdk)
###### 理想效果
![API调用](https://github.com/Yejiejie/API_ML_AI/blob/master/API%E8%B0%83%E7%94%A8.png)
- 车型识别输入![车型识别输入](https://github.com/Yejiejie/API_ML_AI/blob/master/%E8%BD%A6%E5%9E%8B%E8%AF%86%E5%88%AB%E8%BE%93%E5%85%A5.png)
- 车型识别输出![车型识别输出](https://github.com/Yejiejie/API_ML_AI/blob/master/%E8%BD%A6%E5%9E%8B%E8%AF%86%E5%88%AB%E8%BE%93%E5%87%BA.png)
###### 现实调用
- 第一次尝试
![](https://github.com/Yejiejie/API_ML_AI/blob/master/api1.png)
![](https://github.com/Yejiejie/API_ML_AI/blob/master/api2.png)
- 不断尝试
