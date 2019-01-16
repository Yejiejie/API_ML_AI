# API_ML_AI
## 微信小程序

### Product Requirements
|Target release|2018/12/30|
|--------------|----|
|epic|微信小程序——通过拍照识别车型并且能知道该车的销售门店|
|Document Status|已完成|
|Document owner|叶家杰|
|Designer|叶家杰|
|Developer|叶家杰|


### PRD：
#### 1. 背景（用户痛点）：
##### 自身：
- 1.经过调查，到目前为止，大部分人购车都是通过到实体门店试车后才会下决定的。许多汽车APP产品定位都是为用户提供的车型数据等选车方面的服务。但是这些APP并没有提供当地门店的具体位置的功能，即使用户在APP上获取了某款车的资讯，但是对于获得具体的4S门店位置信息还需手动搜索。
- 2.微信作为一个功能强大的综合性应用软件，却不能满足用户通过拍照或者图片得到反馈车辆品牌、型号、介绍等需求。

##### 整体：对于提供上述两个功能的综合运用的应用尚未开发。

#### 2. 战略契合处（加值宣言）：
- 随着移动互联网技术的发展，手机在日常生活中越来越重要。许多事情都能够通过手机完成。随着人们生活水平的提高，车也是成为了人们出行的必需品。一款能够通过拍照识别出车型，并且能根据用户所在地方的推荐该车在当地的销售门店的小程序应用，既能满足用户所想了解的车的相关资料，又能满足到实体店看车的需求。

#### 3.产品概述
- 核心功能（核心价值）：通过拍照/上传图片的方式，最小实现对图片的输出（即车型及相关介绍），并展示用户当地的车在售4S门店的位置，解决看车不知道去哪的问题。

#### Goals（产品目标）
- 1.随时随地，拿起手机，满足用户想要知道车子信息的好奇心。
- 2.并通过查询得到的结果，找寻到相关门店。

#### Assumptions产品使用场景设想（人工智能概率性与用户痛点)：

|#|场景|方式|可行性概率|
|-|---|----|----------|
|1|日常生活中|检测用户上传的车辆图片，识别所属车型，包括车辆品牌及具体型号、颜色、年份、位置信息。|＞95%|
|2|日常生活中|检测图片中出现的所有车辆，返回车辆类型与位置。|＞80%|
|3|日常生活中|通过GPS定位，基站定位，混合定位三种定位模式为用户提供高精度的定位服务|＞95%|

#### Requirements（需求列表与人工智能API加值）:

|#|title|User story|importance|API|
|--------------|----|----|-----|-----|
|1|我该去哪里看车啊|当我在某APP上看中了某汽车，我想了解广州从化的门店是否有这辆车在售，但是我却不知道这些门店的具体位置，也不知道该怎么到这些门店去，我该怎么办？这时候能够通过使用【拍照时车】功能，通过上传该车的图片，通过反馈结果便能够解决这个具体问题。|可行性≥90%|POI抓取|
|2|我想知道这辆车的型号|我今天在学校路上看到一辆很炫的车，我想知道这是什么车型，于是我打开应用里的【拍照识车】功能，了解到这是一款奥迪A3新能源插电式混合动力汽车。|可行性≥90%|车型识别|

#### Not doing: 
路线推荐系统

### 原型：

#### User interaction and design
##### 
##### 1.用户流程图

- 功能：【拍照识车】![功能二：【拍照识图】用户流程图](https://github.com/Yejiejie/API_ML_AI/blob/master/%E3%80%90%E6%8B%8D%E7%85%A7%E8%AF%86%E5%88%AB%E3%80%91%E5%8A%9F%E8%83%BD%E6%B5%81%E7%A8%8B%E5%9B%BE.png)

##### 2.产品原型图
###### 首页
![](https://github.com/Yejiejie/API_ML_AI/blob/master/%E9%A6%96%E9%A1%B5.png)
###### 使用页
![](https://github.com/Yejiejie/API_ML_AI/blob/master/%E4%BD%BF%E7%94%A8%E9%A1%B5.png)
###### 输出页
![](https://github.com/Yejiejie/API_ML_AI/blob/master/%E8%BE%93%E5%87%BA%E9%A1%B5%E9%9D%A2.png)
###### 【门店看车】功能使用页
![](https://github.com/Yejiejie/API_ML_AI/blob/master/%E3%80%90%E9%97%A8%E5%BA%97%E7%9C%8B%E8%BD%A6%E3%80%91%E5%8A%9F%E8%83%BD%E9%A1%B5.png)
##### 3.具体原型文档（含交互）
[原型文档](https://yejiejie.github.io/yuanxing/)

### API&AI

#### 需要用到的API
- 高德地图POI
- 百度细粒度图像识别（车型识别、品牌logo识别）
[链接](http://ai.baidu.com/tech/imagerecognition/fine_grained)

#### API调配输入输出
##### 车型识别
- [技术文档](http://lbsyun.baidu.com/index.php?title=androidsdk)
###### 注意事项
![API调用](https://github.com/Yejiejie/API_ML_AI/blob/master/API%E8%B0%83%E7%94%A8.png)
- 拍摄、上传的图片要不大于4M.对大小也有限制。
- 车型识别输入![车型识别输入](https://github.com/Yejiejie/API_ML_AI/blob/master/%E8%BD%A6%E5%9E%8B%E8%AF%86%E5%88%AB%E8%BE%93%E5%85%A5.png)
- 车型识别输出![车型识别输出](https://github.com/Yejiejie/API_ML_AI/blob/master/%E8%BD%A6%E5%9E%8B%E8%AF%86%E5%88%AB%E8%BE%93%E5%87%BA.png)
###### 现实调用
- 尝试
![](https://github.com/Yejiejie/API_ML_AI/blob/master/api1.png)
![](https://github.com/Yejiejie/API_ML_AI/blob/master/api2.png)
![](https://github.com/Yejiejie/API_ML_AI/blob/master/car_result.png)

#### 试用报告分析&风险分析
##### 使用风险报告
||百度图像识别API|腾讯图片识别API|阿里云图像识别API|
|-|------------|-------------|---------------|
|市场分析|能够完整输出车辆信息|主要运用于图片描述和图片分类，并不能够反馈车辆信息|主要运用于图片识别|
|输入输出限制|免费：500次/天|未认证用户1次/s，认证用户2次/s，企业10次/s|5000次/1年|
|定价|0.7元/千次（0<月计费调用量≤5w|免费|0.0025 元/张|

- 总结：根据限有的资料显示，目前国内仅百度图像识别车辆识别。

##### 使用结果分析

|车型|概率|
|---|----|
|普通轿车|＞95%|
|概念车|低于50%|
|古董车|60%-70%|
|改装车|低于20%|

- 总结：虽然除了普通车型外，其它类似改装车、摩托车等类型的车辆识别信息识别结果正确率不高，但由于百度地图API支持可自行建立车辆信息数据库，是一个比较完整、成熟的体系，可以供使用。

|月调用量（万次|车型识别（元/千次|
|-----------|-----------|
|0<月调用量<=5|3.0|
|5<月调用量<=10|2.8|
|10<月调用量<=20|2.5|
|20<月调用量<=50|2.0|
|50<月调用量<=100|1.8|
|100<月调用量|1.5|

- 总结：对于收费来说价格比较合适，另外，调用失败不计费，性价比较高。

##### 高德地图POI
###### 现实调用

![](https://github.com/Yejiejie/API_ML_AI/blob/master/%E5%A5%A5%E8%BF%AA%E8%B0%83%E7%94%A8%E7%BB%93%E6%9E%9C.png)

#### 试用报告分析&风险分析
##### 百度地图VS高德地图：
首先，本产品目前不进行路线推荐系统，所以对路面状况反馈不纳入参考标准之中，标准针对的是地图的准确性和实时性。
两款软件都曾经出现过更新速度过慢的情况，虽然说两家的数据采集是不一样的，可能会有不一样的重点城市，所以首先城市的差异一定会存在，出现更新慢的情况是很正常的。
但是通过使用比较发现百度地图的离线数据更新非常频繁，感觉几乎每次打开都需要更新，高德地图虽然更新不频繁，但是具体数据却比百度要更新的快一些。
所以选择高德地图作为选择对象。

## 清单
- [PRD](https://github.com/Yejiejie/API_ML_AI/blob/master/PRD.md)
- [原型文档](https://yejiejie.github.io/yuanxing/)
- [python文档](https://github.com/Yejiejie/API_ML_AI/blob/master/car.ipynb)

