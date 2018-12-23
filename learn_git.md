# 安装Git

配置用户名    
$ git config --global user.name "XX"    
配置用户邮箱    
$ git config --global user.email "X@X"    

# 创建版本库

$ mkdir learngit #新建文件夹    
$ cd learngit #进入待定位置    
$ pwd #显示当前位置    

# 添加文件到仓库

$ git add readme.txt #添加文件到仓库    
$ git commit -m "XX" #提交文件到仓库，-M "XX"为修改内容的说明

# 查看仓库状态

$ git status #查看仓库当前的状态    
$ git diff <file>... #查看文件做了什么修改    
$ git add <file> #提交修改到仓库    

# 版本回退

$ git log #查看历史记录    
$ cat <file> #查看文件内容    
$ git reset --hard HEAD^ #回退到上个版本（前提是没有推送到远程库），工作区文件内容会改变，修改HEAD^为上一个，HEAD^^上两个，HEAD~100上一百个  
$ git reflog #查看历史命令
  
命令 git add <file> #是将文件添加到暂存区，文件修改后的内容不执行该命令不会被提交到仓库内。    
  
$ git checkout -- <file> #如果未将修改提交到暂存区，该命令可以回退到上一次add或者commit时的状态。  
$ git reset HEAD readme.txt #如果将修改提交到了暂存区，该命令可以回退到上个版本库的状态。
  
>>> git reset HEAD <file>和git reset --hard HEAD的不同：前者仅撤销暂存区的修改，后者会撤销工作区的修改。

# 创建远程仓库

1. 创建SSH Key    
$ ssh-keygen -t rsa -C "email" #在用户主目录中创建SSH Key。    
2. 在github中添加SSH Key    
3. 关联远程库和本地库    

# 克隆远程库

1. 
