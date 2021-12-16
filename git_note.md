[git笔记链接](https://gitee.com/hongjilin/hongs-study-notes/tree/master/%E7%BC%96%E7%A8%8B_%E5%89%8D%E7%AB%AF%E5%BC%80%E5%8F%91%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0/Git%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0)

# 第一节 操作
## 一、整体操作
1. 进入要管理的目录
2. git init 初始化，让git帮我们管理当前文件夹
3. git status 检测当前目录下文件的状态
4. 三种状态的变化
    - 红色：新增文件 / 修改了原来老文件
  -->   **git add 文件名**
    * 绿色：git已经管理起来了 
  -->   **git commit -m '描述信息'**  
    * 个人信息配置：用户名、邮箱【一次即可】
    * 生成版本
    * 查看版本记录
  -->   **git log**
 --> **git reflog //所有版本号**
<hr>

## 二、具体命令
#### 初始化
    git init

#### 检测当前目录下文件的状态 / 检测版本
    git status

#### 管理文件
    git add index.html
#### 管理全部
    git add .

#### 生成版本v1
    git commit -m 'v1'

#### 查看版本记录
    git log 
    git reflog //所有版本号

#### 回滚
    git reset --hard 版本号

<img src="img\11.png" height='500'>

# 第二节 分支
## 一、分支含义
分支可以给使用者提供多个环境，意味着你可以把你的工作从开发主线上分离开来，以免影响开发主线。

## 二、紧急修复bug方案
<img src='img\2.png'>

## 三、命令总结
#### 查看目前所处的分支
    git branch
#### 创建分支
    git branch 分支名称
#### 切换分支（切换到了新环境）
    git checkout 分支名称
#### 合并分支（可能产生冲突）
    git merge 分支名称
    *注意：先切换分支再合并，要在master环境上操作
#### 删掉分支
    git branch -d 分支名称

## 四、github
```
1.给远程仓库起别名
    git remote add origin 远程仓库地址
2.向远程推送代码(-u 提交默认master分支)
    git push -u origin 分支
或者（手动提交dev分支）
    git push origin dev

```

到公司新电脑上第一次获取代码
```
1.克隆代码
    git clone 远程仓库地址（内部已实现git remote add origin 远程仓库地址）
2.切换分支
    git checkout 分支
```
在公司进行开发
```
1.切换到dev分支进行开发
    git checkout dev
2.把master分支合并到dev[仅一次]
    git merge master
3.修改代码
4.提交代码
    git add .
    git commit -m 'xxx'
    git push origin dev
```
回到家中继续写代码 / 之后再在公司继续开发
```
1.切换到dev分支进行开发
    git checkout dev
2.拉代码
    git pull origin dev
3.继续开发
4.提交代码
    git add .
    git commit -m 'xxx'
    git push origin dev
```

开发完毕，要上线
```
1.将dev分支合并到master，进行上线
    git checkout master
    git merge dev
    git push origin master
2.把dev分支也推送到远程
    git checkout dev
    git merge master
    git push origin dev
```

# 第三节 （p16）
## 一、