## 在ubuntu上安裝git
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

結果如下
```
[master (root-commit) 6e9cc] first commit python
 1 file changed, 1 insertion(+)
 create mode 100644 first.py
```

**3. 檢視交送紀錄**

先修改first.py如下以展示git的功能
```
s = 'fish'
print 'Happy',s
```
再次提交
> $ git add --all

> $ git commit -m 'add fish'

檢視紀錄
> $ git log

結果如下
```
commit 693bf8cfe5b457783e70d4f7cd1927c55e1949ee
Author: Your Name <youremail@domain.com>
Date:   Fri Feb 19 19:38:03 2016 +0800

    add fish

commit 6c4a0bf82b1355318361d9c97df6e179e29bcd23
Author: Your Name <youremail@domain.com>
Date:   Thu Feb 18 22:03:15 2016 +0800

    first commit python
```
查看某一送交的詳細內容
> $ git show 693bf8cfe5b457783e70d4f7cd1927c55e1949ee

檢視不同版本的差異
> $ git diff 6c4a0bf82b1355318361d9c97df6e179e29bcd23 \693bf8cfe5b457783e70d4f7cd1927c55e1949ee

結果如下
```
diff --git a/first.py b/first.py
index 082621b..a51e55b 100644
--- a/first.py
+++ b/first.py
@@ -1 +1,2 @@
-print 'Happy'
+s = 'fish'
+print 'Happy',s
diff --git a/first.py~ b/first.py~
new file mode 100644
index 0000000..636b16c
--- /dev/null
+++ b/first.py~
@@ -0,0 +1,2 @@
+s = 'fish'
+print 'Happy',a
```
## 上傳到git(未完)
> $ git push -u origin master