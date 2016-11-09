###使用uploadify实现上传文件时，发现只要一初始化就会向服务器发出一个网络请求，而这个请求是当前页面的地址，从互联网上找到解决方案：

###原代码片段：

```javascript
this.settings.upload_url = SWFUpload.completeURL(this.settings.upload_url);this.settings.button_image_url = SWFUpload.completeURL(this.settings.button_image_url)
```

###替换后的代码片段：
```javascript
this.settings.upload_url = SWFUpload.completeURL(this.settings.upload_url);this.settings.button_image_url = this.settings.button_image_url ? SWFUpload.completeURL(this.settings.button_image_url) : this.settings.button_image_url
```
