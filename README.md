## Demonstration of how to work with Git?

Here we first create GitHub repository named 'financeproject'. 
We installed git locally and then cloned this this repo to work locally.

**Steps we executed on terminal:**

***1. GIT CLONE <git url>***
```
git clone https://github.com/MS-9web/financeproject.git
cd.. -> one folder back
mkdir <foldername> -> creates folder
ls -> list directory
 ```
>our folder structure is D:\Mishty\DATA ENGINEER\AttackMode\financeproj\financeproject

***2. GIT STATUS***
>For any new file added, will be placed under "untracked files".  
>For existing files, it will be shown under "Changes not staged for commit"
```

PS D:\Mishty\DATA ENGINEER\AttackMode\financeproj\financeproject> git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
 will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        test.py

no changes added to commit (use "git add" and/or "git commit -a")
```
***3.How to commit a change?***

>Whenever we make changes (unstaged) ----> stage (changes are ready to be committed) -----> commit

>Staging the changes:  
>git add .  --> stages all files in current working directory<br>
>git add filename --> stages specified file  
>Commiting the changes:  
>git commit -m "meaningful message"
```
STAGING THE CHANGES:
--------------git terminal output------------------
PS D:\Mishty\DATA ENGINEER\AttackMode\financeproj\financeproject> git add.
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   README.md
        new file:   test.py

COMMITING OUR CHANGES:
D:\Mishty\DATA ENGINEER\AttackMode\financeproj\financeproject>git commit -m "File changes"
[main 07c0406] File changes
 2 files changed, 2 insertions(+)
 create mode 100644 test.py

```
***4.Checking the status after commiting the changes***
>The changes are committed but they are local not on GitHub yet. Local is 1 commit ahead of main.
```
--------------git  terminal output------------------

PS D:\Mishty\DATA ENGINEER\AttackMode\financeproj\financeproject> git status   
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
```
***5. GIT PUSH:***  Pushing changes to GitHub
```
D:\Mishty\DATA ENGINEER\AttackMode\financeproj\financeproject>git push origin main
Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Delta compression using up to 12 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (4/4), 344 bytes | 172.00 KiB/s, done.
Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/MS-9web/financeproject.git
   742974d..07c0406  main -> main
```
***5.Checking the status after pushing the changes***
```
D:\Mishty\DATA ENGINEER\AttackMode\financeproj\financeproject>git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
```
***How to go one commit back?***
```
$ git reset --soft HEAD~1

$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   test.py
        new file:   test.txt
```
