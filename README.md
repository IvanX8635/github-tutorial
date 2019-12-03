## The GitHub Tutorial

_by IVAN_

---
## Git vs. GitHub
Git is a very special system that allows the users to keep track of the changes made by themselves which can be very useful if you want to revert changes. Furthermore, git is used  based on how you save the changes which can be pushed to github where you can collaborate with others with the use of forking and submitting pull requests.


---
# _ Basics of Learning the command line - _
`cd [destination]` - To change your position within your IDE  
`mkdir [file-name]` - Makes a folder followed by a name.  
`mv [file-name] [Existing file name(To move)/new name(To rename)]` - either moves file if the second argument exist or renames the file if the second argument does not exist.
## Initial Setup
1. Get onto the IDE you are using(The command line).
1. Find a place to create a directory which will soon by initialized by git. Typing ``pwd`` will show you where you are and typing ``ls`` will show what files are in the folder you are in right now. You can also look at the right of the console where you can see the place you are in within the entire IDE.
1. Either you create a new directory by using ``mkdir <directory name>`` or have a existing one to work with.
1. cd into the directory you would want to be initialize by git - type : `` cd <directory name>`` try to use tab to autocomplete when you type in something that already exists.  
1. **Now you can finally make the repository to git it running, sorry I just did that. Ready set ! type ``git init``**
1. Congratulations, now you have git running and the folder you are in is now a repository.



---
## Repository Setup
Log in to a cloud (ie. Github)
On the home screen, you can see a button that is called "New" on the right column of the home page.
On the creation tab, give the repo an appropriate and acclimated name. You do not need to do anything else besides creating the repository.

When you first start the repo, you should see HTTPS and SSH key above.
Click on the SSH and copy the URL

Go into the repository you want to be bridge with for github in your IDE. Do ``git remote add [SSH URL]`` and be sure to verify it using ``git remote -v`` to have a verbose way of telling whether you have the remote or not.



---
## Workflow & Commands
Now as you are editing the files and the contents within the repository, you can start to begin to save changes and using the changes later on.
``git add <file-name>`` will add the files to stage. The stage is where you store everything you want to save as a commit later on.
``git add .`` - adds all of the changes to the stage
``git reset HEAD`` will unstage the changes

``git status`` is recommended for starters since it can help you keep track of what has been edited and what has been changed within the repository.

``git commit -m "[message]"`` - Will take a snapshot of whatever is on stage
``git log`` - will show you the previous commits(Very useful)  

``git push`` will save upload the commits to cloud(ie. github)**Must have a remote first! Look at the Repo setup above

---
## Rolling Back Changes
``git revert [SHA]``- Use ``git log`` to see the tag (SHA) - the characters that indicates or identifies a commit. This will allow you to roll back changes with a particular commit.

**Let say you have committed something and want to go back**  
Do ``git log`` within the repo and identify the checkpoint.

You can ``git reset --soft HEAD`` to undo the commit and still have what is on stage one commit previously previously.  

``git reset --hard HEAD`` completely nukes it and resets everything; even what has been added on stage one commit previously.

---

## Errors