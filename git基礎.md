## 再ubuntu上安裝git
**1. 安裝指令**
> $ sudo apt-get update

> $ sudo apt-get install git

**2. 設定名字和電子郵件**
> $ git config --global user.name "Your Name"

> $ git config --global user.email "youremail@domain.com"

## 基礎git操作(未完)
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

加入 first.py
> $ git add first.py

或是一次加入全部檔案
> $ git add --all

顯示容器中的檔案狀態
> $ git status

結果如下
```
On branch master

Initial commit

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)

	new file:   first.py
```
不過上面顯示檔案部必須再經過送交之後才會真正被加入容器

進行提交
> $ git commit -m "first commit python"
```
[master (root-commit) 6e9cc] first commit python
 1 file changed, 1 insertion(+)
 create mode 100644 first.py
```
## 上傳到git(未完)
> $ git push -u origin master