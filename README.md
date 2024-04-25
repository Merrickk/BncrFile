# Bncr_plugins
## 关于企业微信、微信客服和微信公众号适配器的对比说明
### 1.企业微信
**优点：**
采用的是企业微信内的自建应用API，收到消息后可以立即送给后台处理，相对反应更快一点。  
**缺点：**
1.需要设置可信IP，且无法自动更换IP地址，对没有独立的外网IP的用户来说不够友好。  
2.需要用户开通企业微信才能访问应用（开通以后可以在微信端访问）。
### 2.微信客服 
**优点：**
1.不需要设置可信IP。  
2.客服链接可以直接发送给任何微信用户打开。  
3.可以嵌入微信公众号等平台接入。
**缺点：**
适配器采用的是微信客服（独立版）API，收到消息后需要再去腾讯服务器拉取消息，相对来说反应会慢一点。  
### 3.微信公众号 
**优点：**
1.广为人知。  
**缺点：**
1.未认证的订阅号只能在用户发送消息的时候被动回复，不能主动发送消息。  
2.回复消息只能“一问一答”，且需要在收到消息内5秒应答。  
3.回复图片、语音和视频需要添加IP白名单（腾讯系的发送媒体文件都需要上传到服务器）。  

**注意：**
3个适配器都只能1对1使用，无法在群聊中使用（腾讯官方好像也没有提供能在群里使用的API，有的话可以告诉我）