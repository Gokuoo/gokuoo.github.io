![](https://www.runoob.com/wp-content/uploads/2015/02/git-command.jpg)

**说明：**

- workspace：工作区
- staging area：暂存区/缓存区
- local repository：版本库或本地仓库
- remote repository：远程仓库

```
$ git init    
$ git add .    
$ git commit  
```

- git init - 初始化仓库。
- git add . - 添加文件到暂存区。
- git commit - 将暂存区内容添加到仓库中。

## git reset

* git reset --soft

> ①移动本地库HEAD指针

* git reset --mixed  [默认]

> ①移动本地库HEAD指针
> 
> ②暂存区内容放回工作区

* git reset -- hard

> ①移动本地库HEAD指针
> 
> ②重置暂存区
> 
> ③重置工作区

* git reset --keep

> ①移动本地库HEAD指针
> 
> ②暂存区不变
> 
> ③重置工作区

配合 `git push -f` 可以强推HEAD，没有commit的文件不会被提交，随后再进行文件修改正常提交即可。

## 栈区

* git stash

> 未提交的修改（工作区和暂存区）保存至堆栈中

- git stash save [stashMessage]

> 未提交的修改（工作区和暂存区）保存至堆栈中，并作备注

* git stash pop

> 恢复堆栈的文件到工作区

- git stash pop [0/1/2/3]

> 恢复指定堆栈的文件到工作区

* git stash list

> 查看堆栈内容
