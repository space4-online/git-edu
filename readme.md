
本项目为Git培训项目，包括clone, add, commit, fetch, push, checkout, rebase, reset等操作。


相关操作和说明可以看廖雪峰的Git教程。

新同学按照如下要求完成动作。

0. 安装git

参考：https://www.liaoxuefeng.com/wiki/896043488029600/896067074338496

1. **配置SSH Key**

在本地生成ssh-key 的公钥`id_rsa.pub`， 并配置到Github账号中。

2. **clone**

克隆本项目到本地

```sh
git clone git@github.com:space4-online/git-edu.git
```


3. **本地修改**

在目录下新建自己名字的文件夹，并在其中创建一个`readme.md` 的文件，在其中随便写一些内容

4. **提交本地修改至本地仓库**


```sh
# 查看本地修改的文件
git status 

# 添加所有修改到暂存区
git add .

# 提交到本地仓库
git commit -m 'xxxxx'
```

5. **提交到远程分支**

提交到远程仓库，并在仓库新建分支`xxxx`。不要提交到master分支上。


```sh
git push origin HEAD:xxxxx
```

6. **合并本地多次修改记录**

重复两次步骤3和步骤4，产生多个commit记录。

```sh
# 查看本地仓库的提交记录
git log 

# 找到从master上clone下来的commitID
# 合并多次的修改为一个修改
git rebase -i <commitID>

# 强行push到远端仓库，更新对应分支
git push -f origin HEAD:xxxxxx
```


8. **发起合并请求**

在github上发起合并请求，将你创建的新分支合并到master分支上。

7. **从远端同步最新的代码（master分支）到本地**

```sh

git fetch --all

git rebase origin/master

# 查看修改记录
git log
```
