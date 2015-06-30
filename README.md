# gitplay

## lab0
### new files, several check in, then reset back and modify then check in, what is the flow?

---

## 2. git branch
### 2.1 合并分支
* git checkout master and git merge dev.
* 但是还要更新到remote, 所以还要git commit, git push.
*

### 2.2 回退push
### 2.x 删除分支
* local的话就直接在git里面:
    1. git checkout master
    2. git branch -d dev
* remote的话要这样做:
    * 虽然local删除了, 但是remote还是留着的
    * 所以要按照这个[SOF link](http://stackoverflow.com/questions/2003505/delete-a-git-branch-both-locally-and-remotely)
