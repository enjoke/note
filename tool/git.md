# Git Guide
[author]: x  
[date]:	"2017-05-16 17:55:01"  
[email]: enjoke.cn@gmail.com  
[git]:	https://git-scm.com/downloads  

## Git
Git是一个开源的分布式版本控制系统，可以有效、高速的处理从很小到非常大的项目版本管理。
get git from [url][git]

## config
git config 设置和获取仓库或者系统用户下git配置

### 配置级别  
1.	系统级别     `git config --system` 目标文件$(prefix)/etc/gitconfig 
2.	系统用户级别 `git config --global` 目标文件~/.gitconfig
3.	仓库级别	 `git config --local`  目标文件.git/config

### 常用配置
#### 设置用户名、邮箱
```
git config --global user.name "username"
git config --global user.email "your@email.com"
```
#### 设置编辑器
`git config --global core.editor vim`
#### 设置比较器
`git config --global merge.tool vimdiff`
#### 设置默认提交方案
`git config --global commit.template yourfile`
#### 格式化空白

