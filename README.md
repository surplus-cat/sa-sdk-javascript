[![神策数据](https://github.com/sensorsdata/sa-sdk-android/raw/master/docs/logo.png "神策数据")](https://www.sensorsdata.cn/)
<br><br>

[![License](https://img.shields.io/github/license/sensorsdata/sa-sdk-javascript.svg)](https://github.com/sensorsdata/sa-sdk-javascript/blob/master/LICENSE)
[![GitHub release](https://img.shields.io/github/release/sensorsdata/sa-sdk-javascript.svg)](https://github.com/sensorsdata/sa-sdk-javascript/releases)

# sa-sdk-javascript
## 神策简介

[**神策数据**](https://www.sensorsdata.cn/)
（Sensors Data），隶属于神策网络科技（北京）有限公司，是一家专业的大数据分析服务公司，大数据分析行业开拓者，为客户提供深度用户行为分析平台、以及专业的咨询服务和行业解决方案，致力于帮助客户实现数据驱动。神策数据立足大数据及用户行为分析的技术与实践前沿，业务现已覆盖以互联网、金融、零售快消、高科技、制造等为代表的十多个主要行业、并可支持企业多个职能部门。公司总部在北京，并在上海、深圳、合肥、武汉等地拥有本地化的服务团队，覆盖东区及南区市场；公司拥有专业的服务团队，为客户提供一对一的客户服务。公司在大数据领域积累的核心关键技术，包括在海量数据采集、存储、清洗、分析挖掘、可视化、智能应用、安全与隐私保护等领域。 [**More**](https://www.sensorsdata.cn/about/aboutus.html)

## 使用说明
使用方法请参考文档 http://www.sensorsdata.cn/manual/js_sdk.html  
如有疑问请联系邮箱 shengyonggen@sensorsdata.cn  
注意 SDK 可能不完全向前兼容，请查看版本更新说明 [CHANGELOG.md](CHANGELOG.md) ，如果有说明不兼容的话，需要升级神策分析对应的版本    

## 更新日志
请参见 [CHANGELOG.md](CHANGELOG.md)

## 讨论

| 扫码加入神策数据开源社区 QQ 群<br>群号：785122381 | 扫码加入神策数据开源社区微信群 |
| ------ | ------ |
|![ QQ 讨论群](https://raw.githubusercontent.com/richardhxy/OpensourceQRCode/master/docs/qrCode_for_qq.jpg) | ![ 微信讨论群 ](https://raw.githubusercontent.com/richardhxy/OpensourceQRCode/master/docs/qrcode_for_wechat.JPG) |

## 公众号

| 扫码关注<br>神策数据开源社区 | 扫码关注<br>神策数据开源社区服务号 |
| ------ | ------ |
|![ 微信订阅号 ](https://raw.githubusercontent.com/richardhxy/OpensourceQRCode/master/docs/qrcode_for_wechat_subscription_account.jpg) | ![ 微信服务号 ](https://raw.githubusercontent.com/richardhxy/OpensourceQRCode/master/docs/qrcode_for_wechat_service_account.jpg) |


##

用image的src，将数据进行传输

用image的src有个好处就是轻量，并且还支持跨域

打点基本上都用的这个方法进行发送数据

send(data = {}) {
  const image = new Image(1, 1);
  image.onload = function () {
    image = null;
  };
  image.src = `/?${stringify(data)}`;
}

这是network sa.gif的请求url

http://47.111.95.29:8106/sa.gif?project=default&data=eyJkaXN0aW5jdF9pZCI6IjE3MGJjZTNlMWY1NGI1LTA2OGM2OTNmZjRiODZlLWMzODNmNjQtMTg3NDI3NS0xNzBiY2UzZTFmNjk3YiIsImxpYiI6eyIkbGliIjoianMiLCIkbGliX21ldGhvZCI6ImNvZGUiLCIkbGliX3ZlcnNpb24iOiIxLjE0LjIyIn0sInByb3BlcnRpZXMiOnsiJHNjcmVlbl9oZWlnaHQiOjEwMjcsIiRzY3JlZW5fd2lkdGgiOjE4MjUsIiRsaWIiOiJqcyIsIiRsaWJfdmVyc2lvbiI6IjEuMTQuMjIiLCIkbGF0ZXN0X3RyYWZmaWNfc291cmNlX3R5cGUiOiJ1cmznmoRkb21haW7op6PmnpDlpLHotKUiLCIkbGF0ZXN0X3NlYXJjaF9rZXl3b3JkIjoidXJs55qEZG9tYWlu6Kej5p6Q5aSx6LSlIiwiJGxhdGVzdF9yZWZlcnJlciI6InVybOeahGRvbWFpbuino%2BaekOWksei0pSIsInBsYXRmb3JtX3R5cGUiOiJXZWIiLCIkdmlld3BvcnRfcG9zaXRpb24iOjc3LCIkdmlld3BvcnRfaGVpZ2h0Ijo4ODYsIiR2aWV3cG9ydF93aWR0aCI6MTgyNiwiJHVybCI6Imh0dHA6Ly8xOTIuMTY4LjIuMjA6OTgwMC9pbmRleC5odG1sIiwiJHRpdGxlIjoi5Lic57uP5piT572RLee6uOadv%2BWboui0reS6pOaYk%2BW5s%2BWPsCIsIiR1cmxfcGF0aCI6Ii9pbmRleC5odG1sIiwiZXZlbnRfZHVyYXRpb24iOjEyNC42MTgsIiRpc19maXJzdF9kYXkiOnRydWV9LCJhbm9ueW1vdXNfaWQiOiIxNzBiY2UzZTFmNTRiNS0wNjhjNjkzZmY0Yjg2ZS1jMzgzZjY0LTE4NzQyNzUtMTcwYmNlM2UxZjY5N2IiLCJ0eXBlIjoidHJhY2siLCJldmVudCI6IiRXZWJTdGF5IiwiX3RyYWNrX2lkIjo0NzYwNTQ3ODV9&ext=crc%3D657079826

project: default
data: eyJkaXN0aW5jdF9pZCI6IjE3MGJjZTNlMWY1NGI1LTA2OGM2OTNmZjRiODZlLWMzODNmNjQtMTg3NDI3NS0xNzBiY2UzZTFmNjk3YiIsImxpYiI6eyIkbGliIjoianMiLCIkbGliX21ldGhvZCI6ImNvZGUiLCIkbGliX3ZlcnNpb24iOiIxLjE0LjIyIn0sInByb3BlcnRpZXMiOnsiJHNjcmVlbl9oZWlnaHQiOjEwMjcsIiRzY3JlZW5fd2lkdGgiOjE4MjUsIiRsaWIiOiJqcyIsIiRsaWJfdmVyc2lvbiI6IjEuMTQuMjIiLCIkbGF0ZXN0X3RyYWZmaWNfc291cmNlX3R5cGUiOiJ1cmznmoRkb21haW7op6PmnpDlpLHotKUiLCIkbGF0ZXN0X3NlYXJjaF9rZXl3b3JkIjoidXJs55qEZG9tYWlu6Kej5p6Q5aSx6LSlIiwiJGxhdGVzdF9yZWZlcnJlciI6InVybOeahGRvbWFpbuino+aekOWksei0pSIsInBsYXRmb3JtX3R5cGUiOiJXZWIiLCIkdmlld3BvcnRfcG9zaXRpb24iOjY3NSwiJHZpZXdwb3J0X2hlaWdodCI6ODg2LCIkdmlld3BvcnRfd2lkdGgiOjE4MjYsIiR1cmwiOiJodHRwOi8vMTkyLjE2OC4yLjIwOjk4MDAvaW5kZXguaHRtbCIsIiR0aXRsZSI6IuS4nOe7j+aYk+e9kS3nurjmnb/lm6LotK3kuqTmmJPlubPlj7AiLCIkdXJsX3BhdGgiOiIvaW5kZXguaHRtbCIsImV2ZW50X2R1cmF0aW9uIjoxMDk3LjY1NSwiJGlzX2ZpcnN0X2RheSI6dHJ1ZX0sImFub255bW91c19pZCI6IjE3MGJjZTNlMWY1NGI1LTA2OGM2OTNmZjRiODZlLWMzODNmNjQtMTg3NDI3NS0xNzBiY2UzZTFmNjk3YiIsInR5cGUiOiJ0cmFjayIsImV2ZW50IjoiJFdlYlN0YXkiLCJfdHJhY2tfaWQiOjcwNDQ2NTQzNX0=
ext: crc=-272880580