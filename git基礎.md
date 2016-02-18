## 再ubuntu上安裝git
**1. 安裝指令**
> $ sudo apt-get update

> $ sudo apt-get install git

**2. 設定名字和電子郵件**
> $ git config --global user.name "Your Name"

> $ git config --global user.email "youremail@domain.com"

## 基礎git操作
**1. 建立第一個專案目錄(如first_python)**
> $ mkdir first_python

> $ cd first_python

放入一個python檔案
> $ gedit first.py

加入以下程式碼

```python
print 'Happy'
```
將專案目錄轉成git容器
> $ git init

**2. git容器中加入檔案**
> $ git add first.py
