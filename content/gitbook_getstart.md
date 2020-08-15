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
### 发布到github网站
可以将整个项目一起提交到github远程仓库，或者只提交html页面
> 提交整个项目配置方式
```
$git add .
$git commit -m 'init'
$git push -u origin master
```
在github网站上面配置`Settings`->`Options`->`GitHub Pages`->`Source` branch选择master，路径选择html那个页面`docs`

> 只提交html页面配置
可以自己新建一个文件夹`content`用于放置源文件md格式，新建docs文件夹用于放置生成的html文件，再新建`.gitignore`文件配置git忽略文件配置，再推送项目到github