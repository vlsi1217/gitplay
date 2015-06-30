<<<<<<< Updated upstream
# gitplay
<<<<<<< HEAD
=======

<<<<<<< HEAD
---
# git study
## 0. git flow
### 0.0 理清git存在的意义
* git的flow: [link](https://guides.github.com/introduction/flow/)
>>>>>>> 2fde0bd463b3983f30ba2178a98799a136a366ef
=======
## lab0
### new files, several check in, then reset back and modify then check in, what is the flow?

<<<<<<< HEAD
### learn stashing
* usually, when I'm modifing codes, QA asked to look for other branch or history code, I used to store the folder uglyly to another space, then go back to pull. After QA gone, I had to win merge to find all the changes.
>>>>>>> Stashed changes
=======
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
>>>>>>> c85e58c7fd3da25e0caea86cf8b9d05be84e165f


---
```
tzhang@TZHANG-PC ~/Documents/gitplay/gitplay (master)
$ git push origin master
Username for 'https://github.com': vlsi1217
Password for 'https://vlsi1217@github.com':
To https://github.com/vlsi1217/gitplay.git
 ! [rejected]        master -> master (non-fast-forward)
error: failed to push some refs to 'https://github.com/vlsi1217/gitplay.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. Integrate the remote changes (e.g.
hint: 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

tzhang@TZHANG-PC ~/Documents/gitplay/gitplay (master)
$ git pull origin master
From https://github.com/vlsi1217/gitplay
 * branch            master     -> FETCH_HEAD
Auto-merging README.md
CONFLICT (content): Merge conflict in README.md
Automatic merge failed; fix conflicts and then commit the result.

tzhang@TZHANG-PC ~/Documents/gitplay/gitplay (master|MERGING)
$ git status
On branch master
Your branch and 'origin/master' have diverged,
and have 1 and 2 different commits each, respectively.
  (use "git pull" to merge the remote branch into yours)

You have unmerged paths.
  (fix conflicts and run "git commit")

Unmerged paths:
  (use "git add <file>..." to mark resolution)

        both modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")

tzhang@TZHANG-PC ~/Documents/gitplay/gitplay (master|MERGING)
$ git add . -A

tzhang@TZHANG-PC ~/Documents/gitplay/gitplay (master|MERGING)
$ git status
On branch master
Your branch and 'origin/master' have diverged,
and have 1 and 2 different commits each, respectively.
  (use "git pull" to merge the remote branch into yours)

All conflicts fixed but you are still merging.
  (use "git commit" to conclude merge)

Changes to be committed:

        modified:   README.md


tzhang@TZHANG-PC ~/Documents/gitplay/gitplay (master|MERGING)
$ git commit -m "git revert then push to avoid history rewrite"
[master bdd8966] git revert then push to avoid history rewrite

tzhang@TZHANG-PC ~/Documents/gitplay/gitplay (master)
$ git push origin master
Username for 'https://github.com': vlsi1217
Password for 'https://vlsi1217@github.com':
Counting objects: 10, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (4/4), done.
Writing objects: 100% (6/6), 762 bytes | 0 bytes/s, done.
Total 6 (delta 2), reused 0 (delta 0)
To https://github.com/vlsi1217/gitplay.git
   c85e58c..bdd8966  master -> master

tzhang@TZHANG-PC ~/Documents/gitplay/gitplay (master)
```
>>>>>>> 2fde0bd463b3983f30ba2178a98799a136a366ef
