# Github basic rules

![1703465910680](https://github.com/MahinulAbid2/Gtihub-Basic-commands/assets/70069009/31b9e34d-ed91-43b4-a4bc-cc29c3c8d50b)


**rename git branch**
```console
git branch -m old-name new-name
```

<br>
<br>

how to delete git local branch?
```console
git branch -D branch-name
```



## GitHub initial VS code setup
=================================================
> Configuring user information used across all local repositories
* **Setup Username**
```console
git config --global user.name "[theusername_of_your_github_account]"

//Practical Use of the command
git config --global user.name "mahinulabid1"
```

* **Setup Email Address**
```console
git config --global user.email "[theuserEmail_of_your_github_account]"

//Practical Use of the command
git config --global user.name "mahinulabid1@gmail.com"
```
<br>
<br>


## Git repository Initialize command
=======================================================
* **initialize an existing directory as a Git repository**
```console
git init
```

* **Clone a GITHUB repository using Repository Link**
```console
git clone [url]

//Practical Use of this command
git clone https://github.com/mahinulabid1/React-website.git
```

<br>
<br>

## STAGE & SNAPSHOT
======================================================
> Working with snapshots and the Git staging area
* **Show modified files in working directory, staged for your next commit**
>This shows which files are changed and yet needs to be comitted
```console
git status
```
<br>

* **Add a file as it looks now to your next commit (stage)**
```console
git add [file]

//to select all changes. The full stop selects all changes made in the repo
git add .

// select specific file
git add ./filepath/specificFile.extension
```
<br>

* **Unstage a file while retaining the changes in working directory**
```console
git reset [file]

//to reset all files
git reset .

// to reset a specific files
git reset ./filepath/specificFile.extension
```
<br>

* **Diff of what is changed but not staged**
```console
// just this syntax nothing more.
git diff
```
<br>

* **diff of what is changed but not staged**

```console
// just this syntax nothing more.
git diff --staged
```
<br>

* **Commit file with a message**

```console
// just this syntax nothing more.
git commit -m “descriptive message”
```
<br>
<br>
<br>

## BRANCH & MERGE
====================================================
> Isolating work in branches, changing context, and integrating changes

<br>


* **delete local branch**

```console
 git branch --delete branchname
```

* **List your branches. a * will appear next to the currently active branch**

```console
// just this syntax nothing more.
git branch
```
<br>


* **Create a new branch at the current commit**

```console
// just this syntax nothing more.
git branch branch-name
```

<br>

* **Switch to another branch and check it out into your working directory**
```console
git checkout branch-name
```

<br>

* **Merge the specified branch’s history into the current one**
```console
git merge branch_name
```

<br>

* **Show all commits in the current branch’s history**
```console
git log
```

* **Check Remote git branch[Github]. NOT LOCAL branch**
```console
git branch -r
```
> This is just to see how many remote branch are there on GitHub.



### **How to switch remote branch?**

* First fetch the repository. Fetch all.

```console
git fetch
```
NOt mentioning anything after `fetch` will fetch everything.

* Second will be the command for switching the branch.
```console
$ git checkout -t origin/remote-branch-name
```


> `t` stands for `track`. Tt is used to create your branch and setting up the upstream branch automatically to the remote branch.

<br>
<br>
<br>






## SHARE & UPDATE
==================================================================
> Retrieving updates from another repository and updating local repos

<br>

* **Connect to GitHub repository**
```console
git remote add alias url

//practical use
git remote add origin https://github.com/mahinulabid1/React-website.git
```

<br>

* **Fetch down all the branches from that Git remote**
```console
git fetch alias

//practical use
git fetch origin
```

<br>

* **Merge a remote branch into your current branch to bring it up to date**
```console
git merge [alias]/[branch]

//practical use
git merge origin/branch_name
```

<br>

* **Push git branch to the GitHub Repo**
```console
git push [alias] [branch]

//practical use
git push origin branch_name
```

<br>

* **Fetch and merge any commits from the tracking remote branch**
```console
//just this syntax nothing more found on document
git pull
```

<br>
<br>
<br>

## INSPECT AND COMPARE
==============================================================
> Examining logs, diffs and object information
<br>

* **show the commit history for the currently active branch**
```console
//just this syntax nothing more found on document
git log
```
<br>

* **show the commits on branchA that are not on branchB**
```console
git log branchB..branchA
```
<br>

* **show the commits that changed file, even across renames**
```console
git log --follow [file]
```
<br>

* **show the diff of what is in branchA that is not in branchB**
```console
git diff branchB...branchA
```
<br>

* **show any object in Git in human-readable format**
```javascript
git show [SHA]
```
<br>
<br>
<br>
<br>







## TRACKING PATH CHANGES
=============================================================
> Versioning file removes and path changes
> 
<br>

* **show the diff of what is in branchA that is not in branchB** 
```javascript
// remember [file means always file name], remove don't include this [] sign
git rm [file]

//practical use  
git rm index.html
```
<br>

* **change an existing file path and stage the move**
```javascript
git mv [existing-path] [new-path]
```
<br>


* **Show all commit logs with indication of any paths that moved**
```javascript
git log --stat -M
```

<br>
<br> 
<br>
<br>

## REWRITE HISTORY
===========================================================================
> Rewriting branches, updating commits and clearing history
<br>

* **apply any commits of current branch ahead of specified one**
```javascript
git rebase [branch]
```
<br>

* **clear staging area, rewrite working tree from specified commit**
```console
git reset --hard [commit]
```

<br>                
<br>
<br> 
<br>

## TEMPORARY COMMITS
==========================================================================
> Temporarily store modified, tracked files in order to change branches
<br>

* **Save modified and staged changes**
```javascript
git stash
```
<br>

* **list stack-order of stashed file changes**
```console
git stash list
```
<br>

* **write working from top of stash stack**
```javascript
//POP
git stash pop
```
<br>

* **discard the changes from top of stash stack**
```console
//DROP
git stash drop
```
<br>
<br>
<br>
<br>

## IGNORING PATTERNS
=============================================================
> Preventing unintentional staging or commiting of files

<br>

* **Ignore specific Folder**
```console
/filename
```
<br>





