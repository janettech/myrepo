
# myrepo

This README aims to cover how to push code from your local repo with GIT to the remote repo.

## Prerequisite:
The README assumes you have a working local repo initialized with the init command, files staged and committed and ready to push to the remote repo that is GitHub.

## Step1: 
Create a Personal Access Token

You cannot use username and password now.  It is fairly simple to create one. Once done, save your token. You will need it soon.

## Step2: 
You have a local repo on your computer and you want to push a few files to the remote repo.

Check the local branch name with the command `git branch`

It displays as main and not master. Github has changed the naming recently to keep the naming conventions neutral. The default GitHub's branch is main and not master. Accordingly, the push and pull commands must refer to main.

## Step 3: 
Set your remote repo.

`git remote set-url origin <remote-url>`

#### For example: 
The syntax is as 
`https://<personal-access-token-here>@github.com/janettech/myrepo.git`

It took me a while to figure this out, as a google search can give you various ways either through SSH or HTTPS. I have used HTTPS here.

## Step4: 
Confirm that your git-config file must be pointing to the remote-url.

On the terminal, type `vi ./git/config`

The config file is a hidden file. So, if you type `ls -a`, it will show you the hidden files in git.

Confirm that the remote-url is the same as the above.

Edit the file if needed. To save, hit on the `ESC key` and type `:wq` to save and exit.

## Step5: 
Push the files to the remote repo.

`git push -f origin main`

You will see the below output:

	Enumerating objects: 6, done.
	Counting objects: 100% (6/6), done.
	Delta compression using up to 8 threads
	Compressing objects: 100% (5/5), done.
	Writing objects: 100% (6/6), 2.39 KiB | 1.20 MiB/s, done.
	Total 6 (delta 0), reused 0 (delta 0)
	To https://github.com/janettech/myrepo.git
	 * [new branch]      main -> main
 
 ## Step6: 
 Check your Github repo to confirm the uploaded files. Yay!
