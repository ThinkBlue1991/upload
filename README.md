# upload-demo *(include download)*

Uploading a large file by fragmentation, powered by Flask and WebUploader. Downloading the file through streaming.  


## 目的

* 前端采用分片方式上传大文件给后端，后端接收全部分片后，将其组合成一个文件  

* 支持多用户同时上传，互不干扰  

* 支持流式下载文件，低占用内存  


## 安装

* 通过<code>pip install -r requirements</code>安装所需包  


## 运行

### 配置nginx

* cp upload.conf /etc/nginx/conf.d;nginx -t ;nginx -s reload 

### 启动后台服务

* 命令行键入“python3 service.py”启动服务器  

#启动web页面

* 浏览器访问“192.168.4.32:8888”，点击“请选择”按钮，选择文件并上传  



## 效果

* 文件上传成功
![](http://img.my.csdn.net/uploads/201708/27/1503843837_9940.gif)  

* 文件上传失败
![](http://img.my.csdn.net/uploads/201708/27/1503843837_4091.gif)  


## 技术

* Python语言，Flask框架  

* WebUploader分片与上传，Bootstrap渲染上传进度条  


## 参考

* 上传大致思路：  
[blog.csdn.net/jinixin/article/details/77545140](http://blog.csdn.net/jinixin/article/details/77545140)  
  

* 下载案例来源：  
[stackoverflow.com/questions/24318084/flask-make-response-with-large-files](https://stackoverflow.com/questions/24318084/flask-make-response-with-large-files)  
  

* github

[github](https://github.com/jinixin/upload-demo)