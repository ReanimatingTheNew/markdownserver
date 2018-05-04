# markdownServer

## 工程结构

* ./markdowns/* 存放需要解析的markdown文件
* ./templates/* 存放工程需要的html模板

## 接口

* / index显示扫描到的文件列表
* /file/${fileName}/ 显示markdown转换后的HTML页面
* /update 调用后，重新扫描文件目录

## 使用

>由于使用packr将html模板编译入静态文件内，编译后得到的可执行包可以单独使用。

## 运行参数

* -f 配置需要扫描的markdown文件目录，默认为./markdowns;
* -t 配置html模板(目前只有index.html)目录，设置时使用包内编译的默认资源;
* -p 端口

## 编译

* go build ./manager
* go build