# 用Git将本地代码上传到远程仓库



​		github在2020/10/1宣布上的所有新库都将用中性词「main」命名，取代原来的「master」，如果我们通过**git push -u origin master** 方法上传仓库，在github仓库中就会出现一个master的分支。



## 1、为保持一致性，需要将默认的master分支修改到main

\#1.将代码上传到GitHub的默认main分支（新）

1.git --version   #查看版本

2.git config --global init.defaultBranch main  #git在2.28.0上，重新设置git默认分支为main

 

\#2.在执行提交操作即可

```
git init    //工作空间创建.git文件夹（默认隐藏了该文件夹）

git add .    //添加到暂存区

git commit -m "你的提交注释注释"

git remote add origin http://xxxxxxxxx.git    //本地仓库和远程github关联

git pull --rebase origin main  //远程有readme.md，拉一下

git push -u origin main     //代码合并
```



## **2、如果GitHub上的分支在master上**

\#将代码上传到master分支（旧）

```
1.git init    //工作空间创建.git文件夹（默认隐藏了该文件夹）

2.git add .    //添加到暂存区

3.git commit -m "你的提交注释注释"

4.git remote add origin http://xxxxxxxxx.git  //本地仓库和远程github关联

5.git pull --rebase origin master  //远程有readme.md，拉一下

6.git push -u origin master     //上传代码并合并代码
```

 

## 3、也可以将GitHub仓库里的默认的main分支修改成master

![img](file:///C:\Users\80023166\AppData\Local\Temp\ksohtml3080\wps1.png![img](file:///C:\Users\80023166\AppData\Local\Temp\ksohtml3080\wps3.jpg) 

 

## 4、其他一些常用的指令

```
git remote rm origin             //删除已经关联的origin远程库
```

git pull  命令用于从远程获取代码并合并本地的版本。

git pull 其实就是 git fetch 和 git merge FETCH_HEAD 的简写。

git fetch 从远程获取代码库

```
git push     上传代码
```

==git clone==  拷贝个 Git 仓库到本地，让自己能够查看该项目，或者进行修改。

```
 git clone https://github.com/tianqixin/runoob-git-test
```

git checkout []     //切换分支
 

 
