# AcfunSimpleWebScoket
使用acfun通用后端进行一些查询和操作

使用时请对照[后端WebSocket接口](https://github.com/ACFUN-FOSS/acfunlive-backend/blob/main/doc/%E5%90%8E%E7%AB%AFWebSocket%E6%8E%A5%E5%8F%A3.md)

## 界面
![Snipaste_2021-07-30_18-12-06](https://user-images.githubusercontent.com/88189121/127639406-0e35543d-cea7-491c-94cf-789082e1dd29.png)

## 使用
### 下载[acfunlive-backend](https://github.com/ACFUN-FOSS/acfunlive-backend)源码
### 编译运行
```
go build
.\acfunlive-backend.exe -debug
```
如果这一步有问题，可以直接使用[直播工具箱](https://github.com/ACFUN-FOSS/acfunlive-toolbox-client-Public)的可执行文件

*Path:* `\acfunlive-toolbox\resources\app\acbackend.exe`

### 使用浏览器打开[client.html](https://github.com/knia2021/AcfunSimpleWebScoket/blob/main/client.html)
包含3个示例请求：
* 登录
* 查询当前直播间列表
* 查询30天内直播记录（超过90天的直播记录无法查询）
大部分操作都是需要登录的，能查询的信息也大多是当前登录账号的信息
### 执行查询
1. 点击<kbd>打开WebSocket连接</kbd>
2. 点击<kbd>登录</kbd>
3. 点击<kbd>查询直播间列表</kbd>

### 问题
如果发送请求后超过3秒没有响应，需要重新建立一次连接
