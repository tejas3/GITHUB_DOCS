# GitHub Commands


# How to raise GitHub pull request through command line ?

## **Step 1:**
Open terminal where you want to clone your CA repo
Command: git clone  https://github.com/tejas3/GITHUB_DOCS.git

##################################################################################################


 
## **Step 2:** 
Go to GITHUB_DOCS folder which you recently cloned

``` Command: cd GITHUB_DOCS ```
##################################################################################################
 
 
 
## Step 3: 
Select appropriate branch where you want to push your changes

```Command:-  git branch```
           ```git checkout master```
                     


##################################################################################################
 
 
 
## **Step 4:**
Always pull latest changes from the respective branch before start working on any story/defect, otherwise you might face conflicts

```Command: git pull origin master```

##################################################################################################



## **Step 5:**
Create another local branch from  branch
Why? Because if you want to  do parallel development(on multiple stories) in  then single branch is not helpful, you can switch anytime to your locally created branches to work on another story/defect.
Even if you are working on single story/defect I would recommend to create local branch.

Branch needs to be created from master only. Why? Because if you create local branch from anothe branch then that branch code get copied to newly created local branch and it will messed up.

```Command: git checkout -b USXXXXX```

##################################################################################################
 
 
 
## **Step 6:**
Go to code
Start doing your changes, once finished come back to terminal, and check modified files using below command, it will show all the modified files in your directory.

```Command: git status```

##################################################################################################
 
 
 
## **Step 7:** 
To check diff of your file

```Command: git diff origin --color-words```

##################################################################################################
 
 
 
## **Step 8:**
Add(stage) your untracked files using below command

```Command: git add .```

##################################################################################################
 
 
 
## **Step 9:**
Time to commit your changes

```Command: git commit -m "[USXXXXXX]: Story headline"```

##################################################################################################
 
 
 
## **Step 10:**
Check for your successful  commit 

```Command: git log```

##################################################################################################
 
 
 
## **Step 11:**
Create Fork
· What is fork: 
A fork is a copy of a repository that allows you to freely experiment with changes without affecting the original project.
A forked repository differs from a clone in that a connection exists between your fork and the original repository itself.
In this way, your fork acts as a bridge between the original repository and your personal copy where you can contribute back to the original project using Pull request
 
Click on Fork button: 

Copy HTTPS link
 
Now check remote

```Command 1: git remote -v```

Now we have to add upstream which you have copied

```Command 2:  git remote add upstream ```
 
```Command 3: git remote -v```


##################################################################################################
 
 
 
## **Step 12:**
Push your changes on upstream

```Command: git push -u upstream yourBranchName```

##################################################################################################
 
 
 
## **Step 13:**
Go to github you will see pull request popup
Click on Compare & pull request button

 
Alert: Verify your branch which is highlighted by above box
 
Go down on the same page and check your changes, it will show before and after difference
 
Click on Create pull request button

##################################################################################################
 
 
 
 
## **Step 14:**
Select reviewers by clicking 

##################################################################################################
 
 
 
## **Step 15:**
Now you got some comments from reviewers and you have to fix it.
Follow steps:
Step 6
Step 7
Step 8
Step 9
Step 10
Step 12: After this step your changes will reflect in your pull request and it also increment your commit from 1 to 2.

##################################################################################################
 
 
 
## **Step 16:** 
Once your pull request is approved by your reviewers then you have to click on merge pull request button.
 
##################################################################################################
##################################################################################################
 
 You are done! :-)
 
 
 
## How to Cherry pick?

Hg Mercurial graft is equivalent to git cherrypick
If you push your changes in grizzly and you want to graft same changeset in other branch then go to respective branch and fire below command:

```Command: git cherry-pick hashOfYourCommit```

OR    

```git cherry-pick -m 1 hashOfYourCommit```

For eg: git cherry-pick 885c61e65275208b57229aac0dfdf34df98f1
 
 
 
## How to get hash?

```Command: git log```
 
 
 
## How to update on specific commit/apps version?

```Command: git checkout hashOfYourCommit```
