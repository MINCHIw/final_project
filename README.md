# 期末项目

### **PRD 价值主张设计 15%**

#### **PRD1.加值宣言 3%**

- 图像主体检测API：无需用户费神地亲手抠图，会识别用户拍摄到的图片，或是用户从手机相册中上传的图片，快速检测裁剪出图像主题区域。

- 图像风格转换API：轻松将裁剪出来的主题区域转换成卡通画或者素描的风格，使用户能从日常生活中取材，并用作手账的元素之一，使手账内容更贴切自己的生活。

- 图像对比度增强 API：用户如果对图片的对比度不满意，可以利用此进行调整。


#### **PRD2.核心价值 3%**

- 最小可用产品（产品核心价值）为快速检测裁剪出图像主题区域，将其卡通化或者素描化，可以被当做手账的装饰元素进行使用。

#### **PRD3.核心价值与用户痛点 3%**
- 想要画出在日常生活中看见的花卉植物，亦或者是日常物品，景色等，但是绘画技术不好，手残无法画出自己想要的样子的用户
- 当今手账APP只有固定化的手账贴纸，而本款可以让用户另外地去生活中取材，化为自己手账中的元素，记录并发现生活中细小又美好的事物，使手账内容更贴切自己的生活。

#### **PRD4.人工智能概率性与用户痛点 3%**
- 图像主体检测API识别所裁剪的区域，是用户提交或拍摄图片的主要区域，所以如果用户拍摄的几个物体均占整个图像的差不多区域，那么用户想裁出来的区域与api所裁出的会有所偏差。

#### **PRD5.需求列表与人工智能API加值 3%**
|功能|用户案例|重要程度|
|:-|:-:|-:|
|转换成卡通化或素描化的风格|用户想要将日常生活中拍摄到的图片的主体部分，转换为手账中的贴纸，记录在手账中。|很重要|
|抠图功能|用户只想要图片的主体部分，不要背景部分。|很重要|
|增强图片的对比度|用户对拍摄或上传的图片、转换后的贴纸对比度不满意，想要提高或减低图片或贴纸的对比度。|重要|

**用到的API有：**
- 图像主体检测
- 图像风格转换
- 图像对比度增强


### **原型 20%**

#### **原型1.交互及界面设计 5%**

交互及界面设计：在PRD文件中是否有说明且原型是否有做到：交互及界面设计的某个核心交互环节使用了人工智能的加值

#### **原型2.信息设计 5%**

信息设计：在PRD文件中是否有说明且原型是否有做到：信息设计的某个核心信息或设计使用了人工智能的加值

#### **原型3.原型文档 5%**

原型文档：多少程度上有提供MVP可交互的原型文档，供它人在Github上下载使用

#### **原型4.口头操作说明 5%**

口头操作说明：多少程度上在2-3分钟时间限制内，对听众留下了「的确这是个可行丶可用的人工智能加值产品」的印象

### **API 产品使用关键AI或机器学习之API的输出入展示 15%**

#### **API1.使用水平 5%**
- ##### 图像主体检测代码示例
- **输入**
```
import base64

'''
图像主体检测
'''

request_url = "https://aip.baidubce.com/rest/2.0/image-classify/v1/object_detect"
# 二进制方式打开图片文件
f = open('[本地文件]', 'rb')
img = base64.b64encode(f.read())

params = {"image":img,"with_face":1}
access_token = '[调用鉴权接口获取的token]'
request_url = request_url + "?access_token=" + access_token
headers = {'content-type': 'application/x-www-form-urlencoded'}
response = requests.post(request_url, data=params, headers=headers)
if response:
    print (response.json())
```
- **输出**
```
HTTP/1.1 200 OK
x-bce-request-id: 73c4e74c-3101-4a00-bf44-fe246959c05e
Cache-Control: no-cache
Server: BWS
Date: Tue, 18 Oct 2016 02:21:01 GMT
Content-Type: application/json;charset=UTF-8
{
  "log_id": 895582300,
  "result": {
    "width": 486,
    "top": 76,
    "left": 134,
    "height": 394
  }
}
```
---
- ##### 图像效果增强代码示例
- **输入**
```
# encoding:utf-8

import requests
import base64

'''
图像风格转换
'''

request_url = "https://aip.baidubce.com/rest/2.0/image-process/v1/style_trans"
# 二进制方式打开图片文件
f = open('[本地文件]', 'rb')
img = base64.b64encode(f.read())

params = {"image":img}
access_token = '[调用鉴权接口获取的token]'
request_url = request_url + "?access_token=" + access_token
headers = {'content-type': 'application/x-www-form-urlencoded'}
response = requests.post(request_url, data=params, headers=headers)
if response:
    print (response.json())
```
- **输出**
```
{
	"log_id": "6876747463538438254",
	"image": "处理后图片的Base64编码"
}
```
---
- ##### 图像对比度增强代码示例
- **输入**
```
# encoding:utf-8

import requests
import base64

'''
图像对比度增强
'''

request_url = "https://aip.baidubce.com/rest/2.0/image-process/v1/contrast_enhance"
# 二进制方式打开图片文件
f = open('[本地文件]', 'rb')
img = base64.b64encode(f.read())

params = {"image":img}
access_token = '[调用鉴权接口获取的token]'
request_url = request_url + "?access_token=" + access_token
headers = {'content-type': 'application/x-www-form-urlencoded'}
response = requests.post(request_url, data=params, headers=headers)
if response:
    print (response.json())
```
- **输出**
```
{
    "log_id":739539874,
    "image":"处理后图片的Base64编码"
}
```
---

#### **API2.使用比较分析 5%**
- ##### 腾讯的图像主体检测api（图像识别中的图片智能裁剪）
- **输入**
```
https://tiia.tencentcloudapi.com/?Action=CropImage
&ImageUrl=https://test.jpg
&Width=https://test.jpg
&Height=https://test.jpg
&<公共请求参数>
```
- **输出**
```
{
  "Response": {
    "X": 0,
    "Y": 110,
    "Width": 1100,
    "Height": 880,
    "OriginalWidth": 1100,
    "OriginalHeight": 1390,
    "CropResult": 0,
    "RequestId": "bfd478e1-5c94-4e37-ad22-4a5224a09492"
  }
}
```
#### 使用百度API进行图片裁剪：
![百度api](https://upload-images.jianshu.io/upload_images/9776460-1ed830b9ae4b9175.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

#### 使用腾讯API进行图片裁剪：
![腾讯api](https://upload-images.jianshu.io/upload_images/9776460-8f3925baa5e9f5bc.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

- **总结：同一图片，使用百度的图像主题检测api裁剪出来的部分居中，比较腾讯api裁出的主体部分背景更加少，更精确定位并裁出主体部分。**

---


|对比项|腾讯图片智能裁剪API|百度图像主体检测API|
|:-:|:-:|:-:|
|成熟度|文档的代码格式多样，但是许久未更新，有些代码版本已经老旧|文档清晰且详细，并含多种类型代码|
|精确度|识别裁剪的主体部分稍有偏差|识别裁剪出来的主体部分较精确|
|性价比|0 - 1000千次/月，2元/千次	|500次/日免费，免费额度用尽后开始计费，调用失败不计费|

- **总结：综上比较，从成熟度、精确度以及性价比方面综合考量，选择使用百度的图像主体检测API。**


#### **API3.使用后风险报告 5%**

使用后风险报告：在PRD文件中是否有说明且提供连结证据，所使用的API类别的现在及未来发展性，如API市场竞争程度丶输入输出限制丶定价丶及可替代的程序库（改用自己开发的代码及数据库而不用API）等等

#### **API4.加分项 3%**

使用复杂度：用了2个以上[机器学习](http://e.nfu.edu.cn/mod/page/view.php?id=1135 "机器学习")与人工智能的API之输入及输出
