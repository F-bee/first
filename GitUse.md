# Git的使用--如何将本地项目上传到Github

​	    学习Vue的时候，想把代码托管到 **Github** 上，学习了一下 **Github** 的使用，主要参考[廖雪峰-Git教程](https://www.liaoxuefeng.com/wiki/896043488029600)，[CSDN链接](https://blog.csdn.net/zamamiro/article/details/70172900) 将本地项目上传到 **Github** 的步骤总结如下。

### 1.安装

### 2.创建一个本地版本库（一个文件夹）

桌面右键新建文件夹

或者通过 **cmd** 打开命令行窗口，输入 ：

+ `mkdir test`//创建目录

+ `cd test` //进入该文件夹

<img src="C:\Users\FTFk\AppData\Roaming\Typora\typora-user-images\image-20210415092951142.png" alt="image-20210415092951142" style="zoom: 95%;" />



### 3.把这个文件夹变成Git可管理的仓库

使用命令 `git init`

<img src="C:\Users\FTFk\AppData\Roaming\Typora\typora-user-images\image-20210415093129798.png" alt="image-20210415093129798" style="zoom: 90%;" />

会发现test里面多了个.git文件夹，是Git用来跟踪和管理版本库的。它默认是隐藏文件，如果看不到，设置一下隐藏文件可见即可。

<img src="C:\Users\FTFk\AppData\Roaming\Typora\typora-user-images\image-20210415093158748.png" alt="image-20210415093158748" style="zoom: 67%;" />

### 4.把要添加的项目粘贴到该本地Git仓库中

- 复制进来**GithubUse.txt**测试文件

<img src="C:\Users\FTFk\AppData\Roaming\Typora\typora-user-images\image-20210415093349090.png" alt="image-20210415093349090" style="zoom:67%;" />

- 可以通过 `git status` 命令 来查看当前的状态

<img src="C:\Users\FTFk\AppData\Roaming\Typora\typora-user-images\image-20210415093647334.png" alt="image-20210415093647334" style="zoom:92%;" />

此处提示虽然把项目粘贴过来了，但还没有add到Git仓库上

- 通过 `git add .` 把刚才复制过来的测试文件（项目）添加到仓库上
- 并 `git status` 查看当前状态

<img src="C:\Users\FTFk\AppData\Roaming\Typora\typora-user-images\image-20210415094428489.png" alt="image-20210415094428489" style="zoom: 70%;" />

### 5.把项目提交到仓库

- 通过 `git commit -m "example"`把项目提交到仓库

![image-20210415094835533](C:\Users\FTFk\AppData\Roaming\Typora\typora-user-images\image-20210415094835533.png)

-m 后面引号里面是本次提交的注释内容，这个可以不写，但最好写上，不然会报错。 至此，本地Git仓库这边的工作做完了，下面就到了连接远程仓库（也就是连接Github）。

### 6.在Github上创建一个Git仓库

![image-20210415095253499](C:\Users\FTFk\AppData\Roaming\Typora\typora-user-images\image-20210415095253499.png)

### 7.将Git仓库和本地仓库进行关联

- 在本地TEST仓库的命令行输入 `git remote add origin https://github.com/F-bee/TEST.git `

![image-20210415095620817](C:\Users\FTFk\AppData\Roaming\Typora\typora-user-images\image-20210415095620817.png)

![image-20210415095743770](C:\Users\FTFk\AppData\Roaming\Typora\typora-user-images\image-20210415095743770.png)

origin后面加的是上一步Github上创建好的仓库的地址。

### 8.把本地库的内容推送到远程仓库

 `git push -u origin master`

​        由于新建的远程仓库是空的，所以要加上-u这个参数，等远程仓库里面有了内容之后，下次再从本地库上传内容的时候只需下面这样就可以了：

`git push origin master`

![image-20210415095956273](C:\Users\FTFk\AppData\Roaming\Typora\typora-user-images\image-20210415095956273.png)

重新刷新Github页面进入刚才新建的那个仓库里面就会发现项目已经成功上传了

![image-20210415100039578](C:\Users\FTFk\AppData\Roaming\Typora\typora-user-images\image-20210415100039578.png)

## 将本地项目上传到Github的整个过程结束