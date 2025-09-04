# Addvanced Git

## Part one

### Q1
``` bash
PS C:\Users\Cococe Ltd\Advanced-new-Git> git status
On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        test1.md
        test2.md
        test3.md
        test4.md

nothing added to commit but untracked files present (use "git add" to track)

PS C:\Users\Cococe Ltd\Advanced-new-Git> git add test1.md
PS C:\Users\Cococe Ltd\Advanced-new-Git> git commit -m "chore: Create initial file"
[main 7f6a30e] chore: Create initial file
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test1.md
PS C:\Users\Cococe Ltd\Advanced-new-Git> git add test2.md
PS C:\Users\Cococe Ltd\Advanced-new-Git> git commit -m "chore: Create another file"
[main 795cdcc] chore: Create another file
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test2.md
PS C:\Users\Cococe Ltd\Advanced-new-Git> git add test3.md
PS C:\Users\Cococe Ltd\Advanced-new-Git> git commit -m "chore: Create third and fourth files"
>>
[main b861758] chore: Create third and fourth files
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test3.md
PS C:\Users\Cococe Ltd\Advanced-new-Git> git status
On branch main
Your branch is ahead of 'origin/main' by 3 commits.
  (use "git push" to publish your local commits)

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        test4.md

nothing added to commit but untracked files present (use "git add" to track)
PS C:\Users\Cococe Ltd\Advanced-new-Git> git log
commit b861758f14d1a01cd36d418ac829b5fdf718d0a4 (HEAD -> main)
chore: Create third and fourth files, add test4.md
Author: tuyishime eric <erictuyishime2004@gmail.com>
Date:   Thu Sep 4 11:01:31 2025 +0200

    chore: Create third and fourth files

commit 795cdcca943c3fcd851bd422f1fbf3946c5ab394
Author: tuyishime eric <erictuyishime2004@gmail.com>
Date:   Thu Sep 4 11:01:13 2025 +0200

    chore: Create another file

commit 7f6a30eabb719c6843ed9c3002a3c470814f2429
Author: tuyishime eric <erictuyishime2004@gmail.com>
Date:   Thu Sep 4 11:00:57 2025 +0200

    chore: Create initial file

commit 246047ddd33a41f343464ef40fe1408f5b27bbeb (origin/main)
Author: tuyishime eric <erictuyishime2004@gmail.com>
Date:   Thu Sep 4 10:53:45 2025 +0200

    initial project
PS C:\Users\Cococe Ltd\Advanced-new-Git> git add test4.md
PS C:\Users\Cococe Ltd\Advanced-new-Git> git commit --amend
[main c37fa23] chore: Create third and fourth files, add test4.md
 Date: Thu Sep 4 11:01:31 2025 +0200
 2 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test3.md
 create mode 100644 test4.md
PS C:\Users\Cococe Ltd\Advanced-new-Git> 
```


### Q2
``` bash
 PS C:\Users\Cococe Ltd\Advanced-new-Git> git rebase -i HEAD~3
Successfully rebased and updated refs/heads/main.
PS C:\Users\Cococe Ltd\Advanced-new-Git> git rebase -i HEAD~4
Stopped at 795cdcc...  chore: create second file
You can amend the commit now, with

  git commit --amend

Once you are satisfied with your changes, run

  git rebase --continue
PS C:\Users\Cococe Ltd\Advanced-new-Git> git commit --amend
[detached HEAD 1966b0f] chore: create second file
 Date: Thu Sep 4 11:01:13 2025 +0200
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test2.md
PS C:\Users\Cococe Ltd\Advanced-new-Git> git rebase --continue
Successfully rebased and updated refs/heads/main.
PS C:\Users\Cococe Ltd\Advanced-new-Git> git log --online
fatal: unrecognized argument: --online
PS C:\Users\Cococe Ltd\Advanced-new-Git> git log --oneline
6977dc9 (HEAD -> main) adding README file
b58a74b initial project
0c8bc53 chore: Create third and fourth files, add test4.md
1966b0f chore: create second file
7f6a30e chore: Create initial file
246047d initial project
PS C:\Users\Cococe Ltd\Advanced-new-Git> 

```
### Q3
``` bash


```
### Q1
``` bash


```
### Q1
``` bash


```
### Q1
``` bash


```
### Q1
``` bash


```
### Q1
``` bash


<<<<<<< HEAD
=======
```
### Q1
``` bash


```
### Q1
``` bash


>>>>>>> f1780e4 (initial project)
```

