# rest-client
## http请求新工具，抛掉postman
### 优势
postman非常吃内存，rest工具就是一个页面，非常简单实用
### 安装插件rest-client。 goland、vscode都支持
rest-client

### 使用
1. 在项目目录新增rest-api.http文件
2. post请求


        POST {{host}}/operation/partner/orderlist
        Accept: application/json, text/plain, */*
        Cache-Control: no-cache
        Content-Type: application/json;charset=UTF-8
        Token: {{cmsToken}}

        {
          "page": 1,
          "pagesize": 20,
          "position": 1
        }

3. 发送文件

######################upload
### 测试发送文件信息(文件元数据信息查询)
      POST {{host}}/pub/upload
      Cache-Control: no-cache
      token: 1750d42e5cf1a956ef2e3cd9e4a338fa
      Content-Type: multipart/form-data; boundary=WebAppBoundary


      --WebAppBoundary
      Content-Disposition: form-data; name="file"; filename="timg.jpeg"


      < /Users/ocean.z/Downloads/timg.jpeg
      --WebAppBoundary--

