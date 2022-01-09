## 分支

### 列出分支

```
git branch
```

### 切换分支

\*\*

```
git checkout -b (branchname) 命令来创建新分支并立即切换到该分支下，从而在该分支中操作。
```

\*\*

### 删除分支

```
git branch -d (branchname)
```

### 合并分支

**一旦某分支有了独立内容，你终究会希望将它合并回到你的主分支。 你可以使用以下命令将任何分支合并到当前分支中去：**

```
git merge
```

## 添加文件

**git add**

命令可将该文件添加到暂存区。

**添加一个或多个文件到暂存区：**

```
git add [file1] [file2] ...
```

**添加指定目录到暂存区，包括子目录：**

```
git add [dir]
```

**添加当前目录下的所有文件到暂存区：**

```
git add .
```

## 修改 commit message

### 修改最近一次 commit 的信息

\*\*

```
git commit --amend
```

\*\*

### 修改老旧 commit 的信息

```
git rebase -i commitId
```

\*\*

```
r
```

\*\*

### merge 多个 commit

\*\*

```
git rebase -i commitId
```

\*\*

\*\*

```
s
```

\*\*

## 比较差异

### 比较 onstage 与 head 的差异

**git diff --cached**

### 比较工作区与 unstage 的差异

**git diff**

**如果只想比较某个文件**

\*\*git diff -- fileName1 fileName2 ...

## 如何让暂存区恢复成和 HEAD 的一样？

**git reset Head**

**我们平时添加修改文件后。文件会存储在工作区 当使用 git add 后 会添加到 unstage 这个时候如果想要 unstage 恢复成与 head 相同。则需要使用 git reset head**

## 如何让工作区的文件恢复为和暂存区一样？

\*\*

```
git checkout .
```

\*\*

```
git checkout -- fileName1 fileName2
```

## 怎样取消暂存区部分文件的更改？

**git reset Head -- fileName1 fileName2**

## 看看不同提交的指定文件的差异

**git diff branName1 branchName2 比较两个分支的差异**

**git diff branName1 branchName2 -- fileName1 fileName2 比较两个分支的某几个文件的差异**

**git diff commit1 commit2 -- fileName 比较不同 commit 的文件差异**

## 正确删除文件的方法

**git rm fileName**

## 如何指定不需要 Git 管理的文件？

**.gitignore**

**github 提供了一个 repo github/gitignore 针对不同的语言 可以参考**

## 给文件重命名

**method 1 : mv readme readme.md ->git add readme.md->git rm readme**

**method 2: git mv readme readme.md**

## 显示 log

**git log --oneline**

git log

git log -3
