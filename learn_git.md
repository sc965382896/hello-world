# 安装Git

配置用户名 
$ git config --global user.name "XX"  
配置用户邮箱  
$ git config --global user.email "X@X"  

# 创建版本库

新建文件夹   
$ mkdir learngit  
进入待定位置  
$ cd learngit  
显示当前位置    
$ pwd  

# 添加文件到仓库

添加文件到仓库   
$ git add readme.txt  
提交文件到仓库   
$ git commit -m "XX" #-M "XX"为修改内容的说明。  

# 查看仓库状态

查看仓库当前的状态   
$ git status    
查看文件做了什么修改    
$ git diff <file>...    
提交修改到仓库   
$ git add <file>    

# 版本回退

查看历史记录    
$ git log   
查看文件内容    
$ cat <file>    

回退到上个版本（前提是没有推送到远程库   
$ git reset --hard HEAD^ #工作区文件内容会改变，修改HEAD^为上一个，HEAD^^上两个，HEAD~100上一百个   
查看历史命令
$ git reflog    
  
$ git add <file> #是将文件添加到暂存区，文件修改后的内容不执行该命令不会被提交到仓库内。    

$ git checkout -- <file> #如果未将修改提交到暂存区，该命令可以回退到上一次add或者commit时的状态。  
$ git reset HEAD readme.txt #如果将修改提交到了暂存区，该命令可以回退到上个版本库的状态。
  
> git reset HEAD <file>和git reset --hard HEAD的不同：前者仅撤销暂存区的修改，后者会撤销工作区的修改。

# 创建远程仓库

1. 创建SSH Key    
$ ssh-keygen -t rsa -C "email" #在用户主目录中创建SSH Key。    
2. 在github中添加SSH Key    
3. 关联远程库和本地库    
$ git push -u origin master #把原始分支推送到远程库并且将两者关联(-u参数)，之后可以省略-u。    

# 克隆远程库

1. 在github中创建远程库    
2. 在git中输入命令：git clone git@github.com:users_name/<file>.git    
  
# 分支管理

> 每次提交(commit)后，master分支的指针就前移动一步，实质是HEAD指向当前分支。    

$ git branch dev #创建dev分支    
$ git checkout dev #切换到dev分支    
这两个命令相当于：$ git checkout -b dev    

$ git branch #会列出所有的分支，当前分支前会有 * 号    

$ git merge dev #将dev分支合并到当前分支    

$ git branch -d dev #删除dev分支    

