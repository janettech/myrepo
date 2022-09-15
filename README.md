# myrepo

The README will cover how to push code from your local repo with GIT to the remote repo.

Step1: Create a Personal Access Token

Once done, save your token. You will need it soon.

Step2: Assuming, you have a local repo on your computer and have a few files that you want to push to the remote repo.

Check the local branch name with the command `git branch`

It should be main and not master. Github has changed the naming recently to keep the naming conventions neutral.

Step 3: Set your remote repo as below. 

git remote set-url origin <remote-url>

For example: The syntax is as https://<personal-access-token-here>@github.com/janettech/myrepo.git

It took me a while to figure this out, as a google search can give your various ways either through SSH or HTTPS. I have used HTTPS here.

Step4: Confirm your git-config file for the remote-url.

Step5: On the terminal, type vi ./git/config

This is a hidden file so if you type ls -a, it will show you the hidden files in git.

Confirm that the remote-url is the same you set above.

Edit the file if needed, to save hit on the ESC key and type :wq to save and exit.

Step6: Push the files to the remote repo

git push -f origin main

You see the below output:
Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Delta compression using up to 8 threads
Compressing objects: 100% (5/5), done.
Writing objects: 100% (6/6), 2.39 KiB | 1.20 MiB/s, done.
Total 6 (delta 0), reused 0 (delta 0)
To https://github.com/janettech/myrepo.git
 * [new branch]      main -> main
 
 Step7: Check your Github repo to confirm the uploaded files. Yay!
