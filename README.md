# Git 基本概念

### Git 工作区、缓存区/版本库、Git本地仓库、Git远程仓库

- **工作区：**就是你在电脑里能看到的目录。
- **暂存区：**英文叫stage, 或index。一般存放在 ".git目录下" 下的index文件（.git/index）中，所以我们把暂存区有时也叫作索引（index）。
- **版本库：**工作区有一个隐藏目录.git，这个不算工作区，而是Git的版本库。

 ![img](https://www.runoob.com/wp-content/uploads/2015/02/1352126739_7909.jpg) 

### 



### commit、branch、releases

分支、发行版本

团队中的不同的人在不同的分支上开发，不同分支之间是相互隔离的



# Git 基本操作

### 创建仓库

```bash
git init  #在目录中创建新的 Git 仓库。 你可以在任何时候、任何目录中这么做，完全是本地化的。
          # .git 所有有关你的此项目的快照数据都存放在这里。
          
git config --global user.name '用户名' #设置在github仓库主页显示谁提交了该文件
git config --list #查看设置
```



### 分支管理

```bash
git branch#浏览
git branch 标识符#创建分支
git checkout 分支标识符#切换分支
git checkout -b 分支标识符#创建并切换分支

git branch -d (branchname)#删除分支
```

合并分支

```bash
git merge branch_name #合并分支命令。将任何分支合并到当前分支
```

合并冲突

```

```

### Git 标签

 如果你达到一个重要的阶段，并希望永远记住那个特别的提交快照，你可以使用 git tag 给它打上标签。 

 比如说，我们想为我们 项目发布一个"1.0"版本 

> 我们可以用 git tag -a v1.0 命令给最新一次提交打上（HEAD）"v1.0"的标签。 
>
> -a 选项意为"创建一个带注解的标签"。 不用 -a 选项也可以执行的，但它不会记录这标签是啥时候打的，谁打的 
>
> ```bash
> git tag#查看所有标签
> ```

### .gitignore

让Git仓库忽略的文件裂变



### 基本命令

git默认为当前目录

```bash
git status#查看状态。以查看在你上次提交之后是否有修改。
git log #查看提交历史
git help

git add . #.表示当前目录下的所有文件
git rm file_name #删除文件file_name
git commit -m "commit说明"
git commit -m "fix conflict"#解决冲突后提交
git show commit的id
git reset commit的id

git push --set-upstream origin branch_name#push到远端分支branch_name
git pull #拉取远程所有分支代码到本地
git clone 仓库名 本地目录
```

### 快捷键

> t    搜索文件
>
> 



# GitHub Pages

 您可以使用GitHub Pages直接从GitHub存储库托管有关您自己，您的组织或项目的网站。 

### 个人主页

访问：https://用户名.github.io/

搭建步骤

>1.创建仓库。仓库名必须时（用户名.github.io）
>
>2.在仓库下新建index.html文件

### 仓库主页

每个项目创建一个站点

> 1.进入项目主页，点击settings
>
> 2.点击【Lanuch automatic page generator】自动生成主题页面
>
> 3.填写信息，选择主题
>
> 4.访问：https://用户名.github.io/项目名/
>
> 5.修改时的步骤有创建时相同，文件储存在项目的gh-pages分支中

### 自定义404页面

创建新文件。 输入`404.html`或`404.md`。 

 如果您为文件命名`404.md`，请将以下YAML前置事项添加到文件的开头： 

```yml
permalink: /404.html
```

### GitHub  help

 https://help.github.com/ 
