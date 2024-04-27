#  **Git命令(附：CMD常用指令)**

## 一、Git指令

 1. 查看`Git`版本号

 ```git
 git version
 ```

 2. 设置用户名

 ```git
 git config --global user.name "名字" 
 ```

 3. 设置邮箱号码

 ```git
 git config --global user.emal "邮箱号"
 ```

 4. **初始化**当前目录

 ```git
 git init
 ```

5.  将`test.txt`文件加入暂存区

```git
git add test.txt
```

6. 将当前目录的**全部文件**加入暂存区

```git
git add .
```

7. 将当前目录的**全部非隐藏文件**加入暂存区

```git
git add *
```

8. 将当前目录的**全部隐藏文件**加入暂存区

```git
git add .*
```

9. 提交。把暂存区的变为固定的版本，会打开`vim`编辑器，按`a`键或`i`键后进入编辑模式，然后写提交说明，按`esc`键退出编辑模式，输入英文冒号`:`，再输入`wq` （`wq`：表示`write quit`  【翻译为：保存并退出】），回车`Enter`。

```git
git commit
```

10. 简化版的`commit`， 【提交规范为：`git commit -m "fix(test):change content"`】

```git
git commit -m "第二次提交"
```

11. 查看提交信息，会显示每一次的提交信息，每次提交信息都会有一个唯一的`id`标识。

```git
git log 
```

12. 回退到某次提交状态。（参数`id`为每一次提交后得到的唯一`id`，使用`git log`可以查看， 参数`hard`表示覆盖所有变更，同样该参数还可以设置为`soft`， `mixed`模式）

```git
git reset --hard id 
```

## 二、Git分支结构

1. 创建名字为`name`的分支，这里的`name`是自己进行命名的。

```git
git branch name
```

2. 查看所有分支.

```git
git branch -a 
```

3. 切换分支（变更分支）

```git
git checkout '分支名'
```

4. 将分支合并到主分支上。

```git
git merge '分支名'
```

5. 设置推送网址

```git
git remote add origin http://github.com/xxx/xxx.git     # 设置推送网址。
```

6. 删除推送网址

```git
git remote rm origin
```

## 三 、GitHub上的例子

```git
git init

git add REMADE.md

git commit -m "first commit"

git branch -M main     # 创建主分支，并切换到主分支上

git remote add origin http://github.com/midorg-com/re01.git     # 设置推送网址。

git push -u origin main    # 推送到远程仓库，并输入GitHub的邮箱和密码，之后即可推送到远程仓库。
```

## 四、CMD指令

### 常用指令：

 ```powershell
pwd  # 显示当前终端会话所在的目录位置
 ```

 ```powershell
dir  # 显示当前文件夹下的所有文件/文件夹, 可以在后面指定要显示的文件夹的目录结构(如：dir mydir)
 ```

 ```powershell
cd  # 切换目录。【特例：cd .. 切换到上一级目录，cd ../.. 切换到上上一级目录， cd D:  切换到D盘根目录】
 ```

 ```powershell
tree  # 显示当前文件夹下的所有文件的树形结构，可以在后面指定要显示的文件夹的目录结构(如：tree mydir)
 ```

```powershell
shutdown /s /t 3600   # 定时关机, 这里表示3600 秒后关机
```

```powershell
shutdown /a  # 取消关机
```

```powershell
md mydir   # 新建文件夹
rd mydir   # 删除文件夹

echo Hello, World! > newfile.txt  # 创建文件，并输入Hello, World!
del newfile.txt   # 删除文件
```

```powershell
tracert ip/'域名'   # 路由追踪
```

```powershell
ipconfig /flushdns  # 清除本地 DNS 缓存
```

### 进程管理：

```powershell
tasklist   # 显示当前正在运行的进程
start '程序名'   # 运行程序或命令
taskkill /im notepad.exe  # 结束进程，按名称。这里是关闭记事本
taskkill /pid 1234  # 结束进程，按 PID。这里是关闭 PID 为 1234 的进程
```

### 服务管理:

```powershell
net start   		 # 显示当前正在运行的服务：
net start '服务名'   # 启动指定服务：
net stop '服务名'    # 停止指定服务：
```

> 我们可以将常用的命令输入记事本中，并保存为后缀为 `.bat` 的可执行文件。之后只要双击该文件即可执行指定命令，
>
> 或者将文件放入系统`启动`目录中，可以实现开机自动运行。
>
> **启动目录位置**：`C:\Users\用户名\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\Startup`