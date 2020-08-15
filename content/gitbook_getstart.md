# Gitbook使用入门
-----
首先需要nodejs环境

### 安装gitbook-cli 
```
$npm install -g gitbook-cli
```
### 初始化一本书，例如`helloworld`
```
$mkdir ~/helloworld | cd
$gitbook init
```
### 构建，生成html
```
$gitbook build
#或者指定书籍原路径和输出路径
#gitbook build [书籍路径] [输出路径]
$gitbook build ./content ./docs
```
###本地预览
```
$gitbook serve
#或者指定书籍原路径和输出路径
#gitbook serve [书籍路径] [输出路径]
$gitbook serve ./content ./docs
# 指定运行端口 --port
$gitbook serve --port 8080
```
### 生成 PDF 格式的电子书
需要安装Calibre
```
$gitbook pdf ./content ./mybook.pdf
```