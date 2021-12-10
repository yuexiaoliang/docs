# Git

## 文章

[Git:看不到新的远程分支 - IT工具网 (coder.work)](https://www.coder.work/article/184885)
[Git - 打标签 (git-scm.com)](https://git-scm.com/book/zh/v2/Git-基础-打标签)

## Command

```bash
# 克隆指定分支
git clone git@gitee.com:datacenter-han/web-score.git -b mongo mongo

# 分支管理
git branch # 查看本地分支
git branch -r # 查看远程分支
git branch -a # 查看所有分支
git branch -m old_name new_name
git remote prune origin # 清理被删除远程分支在本地库的缓存
git chekcout -b test origin/test # 拉取远程分支(origin/test)到本地分支(test)

# 回滚到之前某一commit
git reset –hard 8ff24a6803173208f3e606e32dfcf82db9ac84d8

# tag 管理
git tag -a v1.0.0 -m "tag 说明" # 添加 tag
git tag -l '*mongo' # 查看所有以 mongo 结尾的 tag
git show v1.0.0 # 查看 tag 信息

# 输出修改最频繁的 50 个文件
git log --pretty=format: --name-only | sort | uniq -c | sort -rg | head -50

# git log 查找关键字
git  log  --grep  隐藏              #检测关键字
git  log  --grep  隐藏 --author yangxyi@kuaiji.com     #检测关键字,并指定关键字作者
```

## 标识

```bash
A: 增加的文件.
C: 文件的一个新拷贝.
D: 删除的一个文件.
M: 文件的内容或者mode被修改了.
R: 文件名被修改了。
T: 文件的类型被修改了。
U: 文件没有被合并(你需要完成合并才能进行提交)
X: 未知状态。(很可能是遇到git的bug了，你可以向git提交bug report)
```

## Commit Message

```bash
# 主要type
feat:     增加新功能
fix:      修复bug

# 特殊type
docs:     只改动了文档相关的内容
style:    不影响代码含义的改动，例如去掉空格、改变缩进、增删分号
build:    构造工具的或者外部依赖的改动，例如webpack，npm
refactor: 代码重构时使用
revert:   执行git revert打印的message

# 暂不使用type
test:     添加测试或者修改现有测试
perf:     提高性能的改动
ci:       与CI（持续集成服务）有关的改动
chore:    不修改src或者test的其余修改，例如构建过程或辅助工具的变动
```