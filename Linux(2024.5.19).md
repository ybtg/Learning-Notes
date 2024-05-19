## 什么是Linux，为什么要用Linux
Linux是一种自由和开放源码的类UNIX操作系统。类似于Windows，各个不同的Linux操作系统称为Linux发行版，Ubuntu是现在使用较为广泛的一个Linux发行版。由于Linux的配置要求低与它的开源性，使得它被许多机载电脑广泛使用，学习Ubuntu可以为后面树莓派等机载电脑的开发打基础。
## Ubuntu20.04换源
参考https://blog.csdn.net/wxd1233/article/details/121779276

1. 进入终端（快捷键Ctrl+Alt+T），备份原来的源
```
sudo cp /etc/apt/sources.list /etc/apt/sources.list.bak
```
2. 再输入以下命令
```
sudo rm /etc/apt/sources.list
sudo nano /etc/apt/sources.list
```

3. 右键粘贴如下配置内容更换源
```
deb http://mirrors.aliyun.com/ubuntu/ focal main restricted universe multiverse 
deb http://mirrors.aliyun.com/ubuntu/ focal-security main restricted universe multiverse 
deb http://mirrors.aliyun.com/ubuntu/ focal-updates main restricted universe multiverse 
deb http://mirrors.aliyun.com/ubuntu/ focal-proposed main restricted universe multiverse 
deb http://mirrors.aliyun.com/ubuntu/ focal-backports main restricted universe multiverse 
deb-src http://mirrors.aliyun.com/ubuntu/ focal main restricted universe multiverse 
deb-src http://mirrors.aliyun.com/ubuntu/ focal-security main restricted universe multiverse 
deb-src http://mirrors.aliyun.com/ubuntu/ focal-updates main restricted universe multiverse 
deb-src http://mirrors.aliyun.com/ubuntu/ focal-proposed main restricted universe multiverse 
deb-src http://mirrors.aliyun.com/ubuntu/ focal-backports main restricted universe multiverse
```
按Ctrl+X退出，按Y保存

4. 再输入命令更新源
```
sudo apt-get update
```
5. 最后输入命令更新一下软件即可
```
sudo apt-get upgrade
```
## Vim的安装与使用
1. Ubuntu20.04安装Vim
```
sudo apt-get install vim
```
2. Vim使用
用光标移动，按
**i**
进入编辑，按
**Esc**
退出编辑，在非编辑状态下，使用
**q!**
不保存强制退出，使用
**wq**
保存并退出
## Linux中各个命令的用法
1. 参考https://www.runoob.com/w3cnote/linux-common-command-2.html

2. 用
**vi [文件名]**
或者
**vim [文件名]**
新建文件，如``vi test.txt``会在当前目录下生成test.txt文件
## 学习建议
1. 不会的命令，用谷歌/必应/百度查一下
2. 遇到报错/警告，去github（https://github.com/） 或者 stackoverflow（https://stackoverflow.com/） 查一下

