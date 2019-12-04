## The GitHub Tutorial

_by IVAN_

---
## Git vs. GitHub
Git is a very special system that allows the users to keep track of the changes made by themselves which can be very useful if you want to revert changes. Furthermore, git is used  based on how you save the changes which can be pushed to github where you can collaborate with others .


---

## Initial Setup
**This is a quick tutorial for getting started on Github**

Sign up for [Github](github.com) Verify if necessary  

Log into a cloud (ie. Github)

Log into a cloud. Example: [CS50](https://ide.cs50.io/)  

The SSH key allows your Github to trust your IDE. You will need your IDE and github account for this.  
Set up an SSH key - [link](https://github.com/hstatsep/ide50) credit to Mr. Mueller
---
## Repository Setup

1. Get onto the IDE you are using(The command line).
1. Find a place to create a directory which will soon by initialized by git. Typing ``pwd`` will show you where you are and typing ``ls`` will show what files are in the folder you are in right now. You can also look at the right of the console where you can see the place you are in within the entire IDE.
1. Either you create a new directory by using ``mkdir <directory name>`` or have a existing one to work with.
1. cd into the directory you would want to be initialize by git - type : `` cd <directory name>`` try to use tab to autocomplete when you type in something that already exists.
1. **Now you can finally make the repository to git it running, sorry I just did that. Ready set ! type ``git init``**
1. Congratulations, now you have git running and the folder you are in is now a repository.

Back on Github, on the home screen, you can see a button that is called "New" on the right column of the home page that should look like a green version of this icon.
![The repo icon](https://upload.wikimedia.org/wikipedia/commons/0/00/Octicons-repo.svg)
On the creation tab, give the repo an appropriate and acclimated name. You do not need to do anything else besides creating the repository.

When you first start the repo, you should see HTTPS and SSH key above.
Click on the SSH and copy the URL

Go into the repository you want to be bridge with for github in your IDE. Do ``git remote add [SSH URL]`` and be sure to verify it using ``git remote -v`` to have a verbose way of telling whether you have the remote or not.

Now you have a repo on the IDE and the repo on Github.

**Now you can add and commit changes which we will discuss below.**

---
## Workflow & Commands
Now as you are editing the files and the contents within the repository, you can start to begin to save changes and using the changes later on.
``git add <file-name>`` will add the files that changed to stage. The stage is where you store everything you want to save as a commit later on.
``git add .`` - adds all of the changes to the stage
``git reset HEAD`` will unstage the changes

``git status`` is recommended for starters since it can help you keep track of what has been edited and what has been changed within the repository.

``git commit -m "[message]"`` - Will take a snapshot of whatever is on stage
``git log`` - will show you the previous commits(Very useful)

``git push`` will save and upload the commits to the cloud repository(ie. github)**Must have a remote first! Look at the Repo setup above

---
## Rolling Back Changes
``git revert [SHA]``- Use ``git log`` to see the tag (SHA) - the characters that indicates or identifies a commit. This will allow you to roll back changes with a particular commit.  
``git checkout [file-name]`` will undo edits within a file  
**Let say you have committed something and want to go back**  
Do ``git log`` within the repo and identify the checkpoint.  
``git reset HEAD~`` will undo the commit in a simple manner  
You can ``git reset --soft HEAD`` to undo the commit and still have what is on stage one commit previously.

``git reset --hard HEAD`` completely nukes it and resets everything; even what has been added on stage one commit previously.

---

## Errors
If you want to uninitialize git you can do ``rm -rf .git`` on the repo.  
Do ``git status`` constantly to keep track of changes made to prevent errors.  
**You can also remove the repo in your IDE and github all together.**  
Go to the parent directory and type in ``rm -rf [repo-name]``  
Go to your the github repo; click on settings and make your way down to the danger zone ; and click delete.   

## Fork/Clone/Pull requests  
This is a way to collaborate or tinker with work from someone else.  
1. On Github you can go into another person's project and fork it. You can click on a icon that looks like this on the mid east of the top of the owner's repo page. ![](https://user-images.githubusercontent.com/17777237/54873012-40fa5b00-4dd6-11e9-98e0-cc436426c720.png)
2. You can then, click on clone button(That large green button). Click on SSH if it is on HTTPS to get the clone URL. After that you can go to your IDE and ``git clone [SSH URL]`` to clone it
3. In the IDE, modifications are allowed for the cloned repo; which means you can add commit and push. 
4. If you would like to suggest a change to the creator, you can submit a pull request by clicking on this icon with the words pull request on it.  
 ![](https://cdn0.iconfinder.com/data/icons/octicons/1024/git-pull-request-512.png)
5. You can create a pull request which will send the suggestions off to the creator. They can accept or deny pull request merge.