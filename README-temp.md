# ADVANCED GIT

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
>>>>>>> 98e387f11eefb01dbb3cf661db221e9f1bfb0bd3

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

### Q4
``` bash
PS C:\Users\Cococe Ltd\Advanced-new-Git> git rebase -i HEAD~9
[detached HEAD 5f1509a] chore: create initial and second file
 Date: Thu Sep 4 11:00:57 2025 +0200
 2 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test1.md
 create mode 100644 test2.md
Successfully rebased and updated refs/heads/main.
PS C:\Users\Cococe Ltd\Advanced-new-Git> git log --oneline
85c9612 (HEAD -> main) readme
09a3b2d adding README file
2801aef adding readme
c725cd4 chore: Create third and fourth files, add test4.md
bf0bc8a adding README file
c81f4dd initial project
7a3cefe chore: Create third and fourth files, add test4.md
5f1509a chore: create initial and second file
246047d initial project
PS C:\Users\Cococe Ltd\Advanced-new-Git> git push origin main --force
>>
Enumerating objects: 25, done.
Counting objects: 100% (25/25), done.
Delta compression using up to 4 threads
Compressing objects: 100% (22/22), done.
Writing objects: 100% (23/23), 3.94 KiB | 310.00 KiB/s, done.
Total 23 (delta 13), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (13/13), done.
To https://github.com/Eric-mar/Git-Advanced.git
 + 563d30b...85c9612 main -> main (forced update)



```

### Q5
``` bash
PS C:\Users\Cococe Ltd\Advanced-new-Git> git log --oneline
34ef194 (HEAD -> main) Update README
b56d8c9 Create Third File
d034b83 Create Fourth File
7f6a30e chore: Create initial file
246047d initial project
PS C:\Users\Cococe Ltd\Advanced-new-Git> git log --oneline
34ef194 (HEAD -> main) Update README
b56d8c9 Create Third File
d034b83 Create Fourth File
7f6a30e chore: Create initial file
246047d initial project
PS C:\Users\Cococe Ltd\Advanced-new-Git> git rebase --abort
>>
fatal: no rebase in progress
PS C:\Users\Cococe Ltd\Advanced-new-Git> git rebase -i 7f6a30e
>>
[detached HEAD fa3a998] Create Third and fourth  File
 Date: Thu Sep 4 23:37:17 2025 +0200
 2 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test3.md
 create mode 100644 test4.md
Successfully rebased and updated refs/heads/main.
PS C:\Users\Cococe Ltd\Advanced-new-Git> git log --oneline
eed964d (HEAD -> main) Update README
fa3a998 Create Third and fourth  File
7f6a30e chore: Create initial file
246047d initial project
PS C:\Users\Cococe Ltd\Advanced-new-Git>

```

### Q6
``` bash
PS C:\Users\Cococe Ltd\Advanced-new-Git> git add .
PS C:\Users\Cococe Ltd\Advanced-new-Git> git commit -m "Unwanted commit"
pick fa3a998 Create Third and fourth  File
[main 0c4fd2d] Unwanted commit
 1 file changed, 4 insertions(+)
 create mode 100644 unwanted.txl
PS C:\Users\Cococe Ltd\Advanced-new-Git> git rebase -i
warning: skipped previously applied commit eed964d
hint: use --reapply-cherry-picks to include skipped commits
hint: Disable this message with "git config set advice.skippedCherryPicks false"        
interactive rebase in progress; onto 98e387f
Last command done (1 command done):
   pick fa3a998 Create Third and fourth  File
Next command to do (1 remaining command):
   drop 0c4fd2d Unwanted commit
  (use "git rebase --edit-todo" to view and edit)
You are currently rebasing branch 'main' on '98e387f'.
  (all conflicts fixed: run "git rebase --continue")

nothing to commit, working tree clean
The previous cherry-pick is now empty, possibly due to conflict resolution.
If you wish to commit it anyway, use:

    git commit --allow-empty

Otherwise, please use 'git rebase --skip'
Could not apply fa3a998... Create Third and fourth  File
PS C:\Users\Cococe Ltd\Advanced-new-Git> git log --oneline
98e387f (HEAD, origin/main, origin/HEAD) Update README
8d2315f Create Fourth File
b56d8c9 Create Third File
d034b83 Create Fourth File
7f6a30e chore: Create initial file
246047d initial project
PS C:\Users\Cococe Ltd\Advanced-new-Git>


```

### Q7
``` bash
PS C:\Users\Cococe Ltd\Advanced-new-Git> git log --oneline
de1b104 (HEAD -> main) Update README
b56d8c9 Create Third File
d034b83 Create Fourth File
7f6a30e chore: Create initial file
246047d initial project
fatal: invalid upstream 'HEAD~4'
PS C:\Users\Cococe Ltd\Advanced-new-Git>  git rebase -i HEAD~3
Successfully rebased and updated refs/heads/main.
PS C:\Users\Cococe Ltd\Advanced-new-Git> git log --oneline
ed952c0 (HEAD -> main) Create Third and fourth File
34b2e1e Update README
7f6a30e chore: Create initial file
246047d initial project
PS C:\Users\Cococe Ltd\Advanced-new-Git>



```

### Q8
``` bash
e07b45c Create Third and fourth File
PS C:\Users\Cococe Ltd\Advanced-new-Git> git branch
* main
PS C:\Users\Cococe Ltd\Advanced-new-Git> git checkout -b ft/branch
Switched to a new branch 'ft/branch'
PS C:\Users\Cococe Ltd\Advanced-new-Git> git add .
PS C:\Users\Cococe Ltd\Advanced-new-Git> git commit -m "Implemented test 5"
[ft/branch 79c303e] Implemented test 5
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test5.md
PS C:\Users\Cococe Ltd\Advanced-new-Git> git push
fatal: The current branch ft/branch has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/branch

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\Cococe Ltd\Advanced-new-Git> git push --set-upstream origin ft/branch
Enumerating objects: 9, done.
Counting objects: 100% (9/9), done.
Delta compression using up to 4 threads
Compressing objects: 100% (7/7), done.
Writing objects: 100% (7/7), 1.69 KiB | 192.00 KiB/s, done.
Total 7 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), done.
remote:
remote: Create a pull request for 'ft/branch' on GitHub by visiting:
remote:      https://github.com/Eric-mar/Git-Advanced/pull/new/ft/branch
remote:
To https://github.com/Eric-mar/Git-Advanced.git
 * [new branch]      ft/branch -> ft/branch
branch 'ft/branch' set up to track 'origin/ft/branch'. PS C:\Users\Cococe Ltd\Advanced-new-Git> git checkout ft/branch   
Already on 'ft/branch'
Your branch is up to date with 'origin/ft/branch'.
PS C:\Users\Cococe Ltd\Advanced-new-Git> git log --oneline
79c303e (HEAD -> ft/branch, origin/ft/branch) Implemented test 5
ed952c0 (main) Create Third and fourth File
34b2e1e Update README
7f6a30e chore: Create initial file
246047d initial project
PS C:\Users\Cococe Ltd\Advanced-new-Git> git checkout main
Switched to branch 'main'
Your branch and 'origin/main' have diverged,
and have 2 and 4 different commits each, respectively.
(use "git pull" if you want to integrate the remote branch with yours)
PS C:\Users\Cococe Ltd\Advanced-new-Git> git cherry-pick 79c303e
[main 1de7c42] Implemented test 5
 Date: Fri Sep 5 01:17:48 2025 +0200
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test5.md
PS C:\Users\Cococe Ltd\Advanced-new-Git> git log --oneline
1de7c42 (HEAD -> main) Implemented test 5
ed952c0 Create Third and fourth File
34b2e1e Update README
7f6a30e chore: Create initial file
246047d initial project
PS C:\Users\Cococe Ltd\Advanced-new-Git>

```

### Q9
``` bash
PS C:\Users\Cococe Ltd\Advanced-new-Git> git log --graph
* commit 1de7c42aa328ea869cadf1bde0497876965b4c87 (HEAD -> main)
| Author: tuyishime eric <erictuyishime2004@gmail.com>
| Date:   Fri Sep 5 01:17:48 2025 +0200
| 
|     Implemented test 5
| 
* commit ed952c0f912d96e54fbcce699f8977f8fa7c4cd2
| Author: tuyishime eric <erictuyishime2004@gmail.com>
| Date:   Thu Sep 4 23:37:17 2025 +0200
| 
|     Create Third and fourth File
| 
* commit 34b2e1e12160e797be14d46d848585a31f693cc5
| Author: tuyishime eric <erictuyishime2004@gmail.com>
| Date:   Thu Sep 4 23:41:30 2025 +0200
| 
|     Update README
| 
* commit 7f6a30eabb719c6843ed9c3002a3c470814f2429
| Author: tuyishime eric <erictuyishime2004@gmail.com>
| Date:   Thu Sep 4 11:00:57 2025 +0200
| 
|     chore: Create initial file
PS C:\Users\Cococe Ltd\Advanced-new-Git>  git cherry-pick --skip
>>
error: no cherry-pick in progress
fatal: cherry-pick failed
PS C:\Users\Cococe Ltd\Advanced-new-Git> git status
On branch main
Your branch and 'origin/main' have diverged,
and have 3 and 4 different commits each, respectively.
  (use "git pull" if you want to integrate the remote branch with yours)

nothing to commit, working tree clean


```

## Part Two
### Q 1&2&3&4
``` bash
PS C:\Users\Cococe Ltd\Advanced-new-Git> git checkout -b ft/new
Switched to a new branch 'ft/new'
PS C:\Users\Cococe Ltd\Advanced-new-Git> git add .
PS C:\Users\Cococe Ltd\Advanced-new-Git> git commit -m "implemented core functionality for the new feature"
[ft/new 2a88784] implemented core functionality for the new feature
 1 file changed, 6 insertions(+)
 create mode 100644 feature.txt
PS C:\Users\Cococe Ltd\Advanced-new-Git> git checkout main
Switched to branch 'main'
Your branch and 'origin/main' have diverged,
and have 3 and 4 different commits each, respectively.
  (use "git pull" if you want to integrate the remote branch with yours)
PS C:\Users\Cococe Ltd\Advanced-new-Git> git add .
PS C:\Users\Cococe Ltd\Advanced-new-Git> git commit -m "Updated project readme"
[main 9030efe] Updated project readme
 1 file changed, 5 insertions(+)
 create mode 100644 readme.txt
PS C:\Users\Cococe Ltd\Advanced-new-Git>


```
### Q5
``` bash
PS C:\Users\Cococe Ltd\Advanced-new-Git> git branch
  ft/branch
  ft/new
* main
PS C:\Users\Cococe Ltd\Advanced-new-Git> git branch -D ft/new
Deleted branch ft/new (was 2a88784).
PS C:\Users\Cococe Ltd\Advanced-new-Git> git branch
  ft/branch
* main
PS C:\Users\Cococe Ltd\Advanced-new-Git> git branch -a
  ft/branch
* main
  remotes/origin/HEAD -> origin/main
  remotes/origin/ft/branch
  remotes/origin/main
PS C:\Users\Cococe Ltd\Advanced-new-Git>   


```

### Q6
``` bash
PS C:\Users\Cococe Ltd\Advanced-new-Git> git log --oneline
9030efe (HEAD -> main, 0a) Updated project readme
1de7c42 Implemented test 5
ed952c0 Create Third and fourth File
34b2e1e Update README
7f6a30e chore: Create initial file
246047d initial project
PS C:\Users\Cococe Ltd\Advanced-new-Git> git checkout -b ft/new-branch-from-commit 34b2e1e
Switched to a new branch 'ft/new-branch-from-commit'
PS C:\Users\Cococe Ltd\Advanced-new-Git> git branch
  0a
  ft/branch
* ft/new-branch-from-commit
  main
PS C:\Users\Cococe Ltd\Advanced-new-Git> git status
On branch ft/new-branch-from-commit

```
### Q7
``` bash
PS C:\Users\Cococe Ltd\Advanced-new-Git> git checkout main
Switched to branch 'main'
Your branch and 'origin/main' have diverged,
and have 4 and 4 different commits each, respectively.
  (use "git pull" if you want to integrate the remote branch with yours)
PS C:\Users\Cococe Ltd\Advanced-new-Git> git merge ft/new-branch-from-commit
Already up to date.
PS C:\Users\Cococe Ltd\Advanced-new-Git> git commit
On branch main
Your branch and 'origin/main' have diverged,
and have 4 and 4 different commits each, respectively.

nothing to commit, working tree clean
PS C:\Users\Cococe Ltd\Advanced-new-Git> git log --oneline --graph --decorate --all
* 9030efe (HEAD -> main, 0a) Updated project readme
* 1de7c42 Implemented test 5
| * 79c303e (origin/ft/branch, ft/branch) Implemented test 5
|/  
* ed952c0 Create Third and fourth File
* 34b2e1e (ft/new-branch-from-commit) Update README
| * 98e387f (origin/main, origin/HEAD) Update README
| * 8d2315f Create Fourth File
| * b56d8c9 Create Third File
| * d034b83 Create Fourth File
|/  
* 7f6a30e chore: Create initial file
* 246047d initial project
PS C:\Users\Cococe Ltd\Advanced-new-Git> 

```
### Q 8 & 9
``` bash
PS C:\Users\Cococe Ltd\Advanced-new-Git> git branch -m  ft/new-branch-from-commit ft/improved-branch-name 
PS C:\Users\Cococe Ltd\Advanced-new-Git> git branch
  0a
  ft/branch
* ft/improved-branch-name
  main
PS C:\Users\Cococe Ltd\Advanced-new-Git> git push origin ft/improved-branch-name
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
remote: 
remote: Create a pull request for 'ft/improved-branch-name' on GitHub by visiting:      
remote:      https://github.com/Eric-mar/Git-Advanced/pull/new/ft/improved-branch-name  
remote: 
To https://github.com/Eric-mar/Git-Advanced.git
 * [new branch]      ft/improved-branch-name -> ft/improved-branch-name
PS C:\Users\Cococe Ltd\Advanced-new-Git> git push origin --delete ft/new-branch-from-commit
To https://github.com/Eric-mar/Git-Advanced.git
 - [deleted]         ft/new-branch-from-commit
PS C:\Users\Cococe Ltd\Advanced-new-Git> git push --set-upstream origin ft/improved-branch-name
>> 
branch 'ft/improved-branch-name' set up to track 'origin/ft/improved-branch-name'.
Everything up-to-date
PS C:\Users\Cococe Ltd\Advanced-new-Git> 

```
### Q10
``` bash
PS C:\Users\Cococe Ltd\Advanced-new-Git> git log --oneline
>> 
9030efe (HEAD -> ft/improved-branch-name, origin/ft/improved-branch-name, main, 0a) Updated project readme
1de7c42 Implemented test 5
ed952c0 Create Third and fourth File
34b2e1e Update README
7f6a30e chore: Create initial file
246047d initial project
PS C:\Users\Cococe Ltd\Advanced-new-Git> git checkout ed952c0
>> 
Note: switching to 'ed952c0'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at ed952c0 Create Third and fourth File
PS C:\Users\Cococe Ltd\Advanced-new-Git> git status
>>
HEAD detached at ed952c0
nothing to commit, working tree clean
PS C:\Users\Cococe Ltd\Advanced-new-Git>   

```

## Part Three
### Q1&2
``` bash

PS C:\Users\Cococe Ltd\Advanced-new-Git> git add .
PS C:\Users\Cococe Ltd\Advanced-new-Git> git stash
Saved working directory and index state WIP on main: 9030efe Updated project readme
PS C:\Users\Cococe Ltd\Advanced-new-Git> git stash pop
On branch main
Your branch and 'origin/main' have diverged,
and have 4 and 4 different commits each, respectively.
  (use "git pull" if you want to integrate the remote branch with yours)

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   stash2.html

Dropped refs/stash@{0} (505ca78b5beffd234f243c0ef3cfe817b390cf6f)
PS C:\Users\Cococe Ltd\Advanced-new-Git>

```
### Q3
``` bash
PS C:\Users\Cococe Ltd\Advanced-new-Git> git add cnflicts.txt
PS C:\Users\Cococe Ltd\Advanced-new-Git> git commit -m "editing on main"
[main 354bdb8] editing on main
 1 file changed, 1 insertion(+), 1 deletion(-)
PS C:\Users\Cococe Ltd\Advanced-new-Git> git checkout new-feature-branch
Switched to branch 'new-feature-branch'
PS C:\Users\Cococe Ltd\Advanced-new-Git> git add cnflicts.txt
PS C:\Users\Cococe Ltd\Advanced-new-Git> git commit -m "editing on new-feature"
[new-feature-branch 7abb3a6] editing on new-feature
 1 file changed, 4 insertions(+)
 create mode 100644 cnflicts.txt
PS C:\Users\Cococe Ltd\Advanced-new-Git> git checkout main               
Switched to branch 'main'
Your branch is ahead of 'origin/main' by 4 commits.
  (use "git push" to publish your local commits)
PS C:\Users\Cococe Ltd\Advanced-new-Git> git merge new-feature-branch
Auto-merging cnflicts.txt
CONFLICT (add/add): Merge conflict in cnflicts.txt
Automatic merge failed; fix conflicts and then commit the result.
PS C:\Users\Cococe Ltd\Advanced-new-Git> git add .
PS C:\Users\Cococe Ltd\Advanced-new-Git> git commit -m "after merging the conflicts"
[main 4da5731] after merging the conflicts
PS C:\Users\Cococe Ltd\Advanced-new-Git>

```

### Q4
``` bash
PS C:\Users\Cococe Ltd\Advanced-new-Git> git checkout 354bdb8a504f3c7410952371790f20d9a2d206be
HEAD is now at 354bdb8 editing on main
PS C:\Users\Cococe Ltd\Advanced-new-Git> git commit -m "testing commit in the detached state" 
HEAD detached at 354bdb8
nothing to commit, working tree clean
PS C:\Users\Cococe Ltd\Advanced-new-Git> git checkout -b fix-detached-head              
Switched to a new branch 'fix-detached-head'
PS C:\Users\Cococe Ltd\Advanced-new-Git>

```
### Q6
``` bash
PS C:\Users\Cococe Ltd\Advanced-new-Git> echo /tmp > .gitignore  
PS C:\Users\Cococe Ltd\Advanced-new-Git> git status
On branch main
Your branch is ahead of 'origin/main' by 6 commits.
  (use "git push" to publish your local commits)

Untracked files:
  (use "git add <file>..." to include in what will be committed) 
        .gitignore

nothing added to commit but untracked files present (use "git add" to track)
PS C:\Users\Cococe Ltd\Advanced-new-Git> git add .
PS C:\Users\Cococe Ltd\Advanced-new-Git> git commit -m "add .gitignore file "
[main 68089ed] add .gitignore file
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 .gitignore
PS C:\Users\Cococe Ltd\Advanced-new-Git> git status
On branch main
Your branch is ahead of 'origin/main' by 7 commits.
  (use "git push" to publish your local commits)

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)

no changes added to commit (use "git add" and/or "git commit -a")PS C:\Users\Cococe Ltd\Advanced-new-Git> git status
On branch main
Your branch is ahead of 'origin/main' by 7 commits.
  (use "git push" to publish your local commits)

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   .gitignore

no changes added to commit (use "git add" and/or "git commit -a")PS C:\Users\Cococe Ltd\Advanced-new-Git> git add .
PS C:\Users\Cococe Ltd\Advanced-new-Git> git status
On branch main
Your branch is ahead of 'origin/main' by 7 commits.
  (use "git push" to publish your local commits)

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   .gitignore

PS C:\Users\Cococe Ltd\Advanced-new-Git> git commit -m "adding an ignore file"
[main 3a872af] adding an ignore file
 1 file changed, 0 insertions(+), 0 deletions(-)


```

### Q 7 & 8
``` bash
PS C:\Users\Cococe Ltd\Advanced-new-Git> git tag v1.0
PS C:\Users\Cococe Ltd\Advanced-new-Git> git tag v2.0
PS C:\Users\Cococe Ltd\Advanced-new-Git> git tag eric
PS C:\Users\Cococe Ltd\Advanced-new-Git> git tag
eric
v1.0
v2.0
PS C:\Users\Cococe Ltd\Advanced-new-Git> git tag -d eric
Deleted tag 'eric' (was a435f8f)
PS C:\Users\Cococe Ltd\Advanced-new-Git> git tag v2.0
fatal: tag 'v2.0' already exists
PS C:\Users\Cococe Ltd\Advanced-new-Git> git tag -d v2.0
Deleted tag 'v2.0' (was a435f8f)
PS C:\Users\Cococe Ltd\Advanced-new-Git> git tag -d v1.0 
Deleted tag 'v1.0' (was a435f8f)
PS C:\Users\Cococe Ltd\Advanced-new-Git>

```

### Q9
``` bash
PS C:\Users\Cococe Ltd\Advanced-new-Git> git branch
  0a
  feature-branch
  fix-detached-head
  ft/branch
  ft/improved-branch-name
* main
  new-feature-branch
PS C:\Users\Cococe Ltd\Advanced-new-Git> git remote -v
origin  https://github.com/Eric-mar/Git-Advanced.git (fetch)
origin  https://github.com/Eric-mar/Git-Advanced.git (push)

```

### Q10
``` bash

```





