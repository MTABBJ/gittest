## 1.1 第一阶段操作
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

<hr>
### 1.2 具体语句
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

