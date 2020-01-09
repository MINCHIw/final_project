# 期末项目

---

| Title | content |
| --- | --- |
| Target release(发布日期) | 2019/12/11|
| Epic(史诗名称) | 沿路手账（可以记录下生活中细小事物的手账制作APP） |
| Document status(文档状态) | 已基本完成 |
| Document owner( 文件的主人) |叶倩晖|
| Designer( 领头的设计师) |叶倩晖|
| Developer( 领头的开发者) |叶倩晖|
| QA(领头的测试者) |叶倩晖|

---

## **一、PRD 价值主张设计**

### **PRD1.加值宣言**

- 图像主体检测API：无需用户费神地亲手抠图，会识别用户拍摄到的图片，或是用户从手机相册中上传的图片，快速检测裁剪出图像主题区域。

- 图像风格转换API：轻松将裁剪出来的主题区域转换成卡通画或者素描的风格，使用户能从日常生活中取材，并用作手账的元素之一，使手账内容更贴切自己的生活。

- 图像对比度增强 API：用户如果对图片的对比度不满意，可以利用此进行调整。

- 人像动漫化 API：用户可以上传人物相关的图片，获得动漫二次元人像效果的人物照片，并将其化为手账元素使用到其中。


### **PRD2.核心价值**

- 最小可用产品（产品核心价值）为快速检测裁剪出图像主题区域，将其卡通化或者素描化，也可以拍摄人物相关的图片，将人物图像1：1 生成动漫二次元人像效果的照片，以上生成的图片均可以被当做手账的装饰元素进行使用。

### **PRD3.核心价值与用户痛点**
- 想要画出在日常生活中看见的花卉植物，亦或者是日常物品，景色等，但是绘画技术不好，手残无法画出自己想要的样子的用户
- 当今手账APP只有固定化的手账贴纸，而本款可以让用户另外地去生活中取材，化为自己手账中的元素，记录并发现生活中细小又美好的事物，使手账内容更贴切自己的生活。
- 用户想要按照现实人物画出二次元形象的人但是身为“手残党”无法画出好看的二次元人物图，无法将其记录在手账中

### **PRD4.人工智能概率性与用户痛点**
- 图像主体检测API识别所裁剪的区域，是用户提交或拍摄图片的主要区域，所以如果用户拍摄的几个物体均占整个图像的差不多区域，那么用户想裁出来的区域与api所裁出的会有所偏差。

### **PRD5.需求列表与人工智能API加值**
|功能|用户案例|重要程度|
|:-:|:-:|:-:|
|转换成卡通化或素描化的风格|用户想要将日常生活中拍摄到的图片的主体部分，转换为手账中的贴纸，记录在手账中。|很重要|
|抠图功能|用户只想要图片的主体部分，不要背景部分。|很重要|
|增强图片的对比度|用户对拍摄或上传的图片、转换后的贴纸对比度不满意，想要提高或减低图片或贴纸的对比度。|重要|
|将人物图像1：1 生成动漫二次元人像效果|用户为“手残党”，较难画出二次元形象的人物图像|重要|

**用到的API有：**
- 图像主体检测
- 图像风格转换
- 图像对比度增强
- 人像动漫化


## **二、原型**
#### **（一）原型源文件**下载地址：[https://gitee.com/NFUNM093/prototype](https://gitee.com/NFUNM093/prototype)

#### **（二）**[Axure高保真原型](http://nfunm093.gitee.io/prototype/#g=1&p=%E9%A6%96%E9%A1%B5)


#### **（三）产品原型图**
#### **1. 首页**
- **首页界面**

![首页](https://upload-images.jianshu.io/upload_images/9776460-15b56d7c6ff7942c.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

---

#### **2. 取材界面**

- **拍照页面**

![拍照界面](https://upload-images.jianshu.io/upload_images/9776460-0ef9585290507f72.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


- **上传照片页**

![上传照片页](https://upload-images.jianshu.io/upload_images/9776460-0b3a31c438709f50.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

- **处理图片界面**

![转换卡通风的界面](https://upload-images.jianshu.io/upload_images/9776460-4fadac9f44533cbe.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![人物二次元转换界面](https://upload-images.jianshu.io/upload_images/9776460-3bd34da515f6830f.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


---

#### **3. 我的**

![我的](https://upload-images.jianshu.io/upload_images/9776460-2cf14e54732ca59c.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

---

#### **（四）产品结构图**

![沿路手账产品结构图.png](https://upload-images.jianshu.io/upload_images/9776460-f4c779b08114a6fb.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


#### **（五）口头操作说明**

- 用户可以在**“取材”**界面使用照相机，拍摄日常生活中的图片，软件会检测裁剪出图像主题区域；
- 接着用户可以将刚才裁剪出来的主题区域转换成卡通画或者素描的风格，这样就得到了装饰手账的一个材料啦。
- 其次，如果用户需要对图片的对比度进行调整，也可以通过**“调整对比度”**进行相应的调整。
- 用户可以拍摄或上传人物图片，会按照1：1 比例生成动漫二次元人像效果，可用于手账元素，用户只需上传图片，即可立刻获得千人千面的动漫人像。
- 在首页可以找到自己平时创建的手账以及素材库，还可以在社区内与其他用户交流分享各自的素材。
- 这个手账中的元素可以由用户自己拍摄，制作属于自己的特别手账，记下用户生活沿路的风景事物，便于用户在未来的某日翻看手账时，也能通过手账中的特别元素与记录的语句，回忆起当时的感受。


## **三、API 产品使用关键AI或机器学习之API的输出入展示**

### **API1.使用水平**
- #### 图像主体检测代码示例
- **输入**
``` python 
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
``` python
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
- #### 图像效果增强代码示例
- **输入**
``` python
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
``` python
{
	"log_id": "6876747463538438254",
	"image": "处理后图片的Base64编码"
}
```
---
- #### 图像对比度增强代码示例
- **输入**
``` python
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
``` python
{
    "log_id":739539874,
    "image":"处理后图片的Base64编码"
}
```

---
- #### 人像动漫化代码示例
- **输入**
``` python
# encoding:utf-8

import requests
import base64

'''
人像动漫化
'''

request_url = "https://aip.baidubce.com/rest/2.0/image-process/v1/selfie_anime"
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
``` python
{
     "log_id":739539874,
     "image":base64str
}
```
---



### **API2.使用比较分析**
- ##### 腾讯的图像主体检测api（图像识别中的图片智能裁剪）
- **输入**
``` python
https://tiia.tencentcloudapi.com/?Action=CropImage
&ImageUrl=https://test.jpg
&Width=https://test.jpg
&Height=https://test.jpg
&<公共请求参数>
```
- **输出**
``` python
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


### **API3.使用后风险报告**

> 中国搜索引擎巨头 **百度** 表示，其新近研发的超级计算机Minwa在一项备受关注的人工智能基准测试ImageNet中取得了世界最好成绩，错误率仅为4.58%，**超越了微软和谷歌的超级计算机。**([资料来源](http://news.mydrivers.com/1/429/429334.htm))

||腾讯图片智能裁剪API|百度图像主体检测API|
|:-:|:-:|:-:|
|市场竞争程度|现已用于天天P图|可应用于含美图功能app等业务场景中，现已用于铺美美智能设计平台|
|输入输出限制|0 - 1000千次/月，2元/千次|免费：500次/天|

**腾讯图片智能裁剪API定价：**

|调用次数|腾讯图片智能裁剪API|
|:-:|:-:|
|0 - 1000千次/月|2元/千次|
|1000千 - 3000千次/月|1.5元/千次|
|3000千 - 15000千次/月|1.2元/千次|
|15000千次以上/月|1元/千次|

**百度图像主体检测API定价：**

|月调用量（万次）|百度图像主体检测API|
|:-:|:-:|
|0<月调用量<=5|0.70元/千次|
|5<月调用量<=10|0.60元/千次|
|10<月调用量<=20|0.50元/千次|
|20<月调用量<=50|0.40元/千次|
|50<月调用量<=100|0.35元/千次|
|100<月调用量|0.30元/千次|

