# GitHub Tutorial

_by Mariam Saleh_

---
## Git vs. GitHub

Git is a version control system that runs in the command line which means that it keeps track of different verions of your code and save the changes you make to your files. However, Github is where you make repositories which is where you save your code forever, so if something happened to your git workspace for some reason, your code and files are always saved on Github. Git doesn't require Github to work, but Github requires Git. 

---
## Initial Setup

In order to start coding, you need to set up a Github account.
Here is how you do it in steps:
1. go to [github sign up page](https://github.com/join?source=header-home).
2. create a username and put your email with a passoword of your preference (if you are an HSTAT student, please use your HSTAT email and passoword).
3. Make sure to click on free account, unless you want to pay money for more features.

After making an account we switch from HTTPS key to SSH (**S**ecure **SH**ell) key.   
The reason we do this is because when you git to push or clone which we will get to later on, we only need to enter our username and password only once.   
Using HTTPS will ask you to enter your password everytime you type a URL while coding. On the other hand, using SSH will let you enter your username and password only once while setting it up, so you won't have to enter it every single time you write a URL.

Taking that into consideration, here are the steps of switching from HTTPS key to SSH key:
1. Got to [github.com](github.com) and sign in
2. Click on the top right profile icon and go to settings
3. In settings, click on **SSH and GPG** on the left
4. Click on **New SSH key**
5. If you are using [Cloud9](c9.io) as your git workspace, go ahead and put Cloud9 as your title
6. Go to your Cloud9 and sign in (if you don't have an acount, go ahead and make one)
7. Click on the top right gear icon and then click on **SSH Keys** 
8. Copy and past the second SSH key into github as your key if you want it to be private
9. Click on **Add SSH key**
10. Go back into your Cloud9 and open your workspace
11. Type **SSh -T git@github.com**

Then, You are done with your initial setup!

---
## Repository Setup

After setting up your account and switching to an SSH key, you need to set up a repository. We do this because we need every change and commit we make to be saved in those repositories forever.

To make a repository in github, called a remote, you need to follow the steps below:
1. Go to your git workspace ([cloud9](c9.io) if you are using it)
2. Make a directory and a file where you will put your work in (if you don't know how to do that, search "**Command Line**")
3. Go to [github.com](github.com) and sign in
4. Click on the plus sign (+) at the top right corner
5. Click on **New Repository** 
6. Give the repository a name (a helpful suggestion is to give your repo the same name as your directory you made earlier)
7. Leave everything else the same and click on **Create Repository**

Now you've made a new repository, you need to do some coding and save your code to the repository you made.

* First, make some edits and writing to your file.
* To start adding and saving all those changes, you need to initialize git in your directory to make it ready to accept any git commands. We do this **only once** at the beginning.
    * To initialize git, type **`git init`** in the the directory you are working in 
* After initializing git or starting it up, you need to add the changes you made to the staging area, making it ready to be saved (aka committed) 
    * To add those changes to the staging area, you need to type **`git add filename`** (filename = the name you gave to your file)
    * Did you know that there are shortcuts with adding that you can take? Well, you can type **`git add .`** which will add all new and modified files that are changed, or you can type **`git add --all`** which will add all changes files, including new, modified, renamed, and deleted files. (`git add .` does NOT add any renamed or deleted files)
* After adding, we commit our changes which means saving them, but they don't go up to the repository we made yet (think of it as taking a screenshot of your work, but you still need to save this screenshot permenantly on your computer which will be github in this case!).
    * To commit your changes, type **`git commit -m "short message"`** (short message = a very short and specific message you give to yourself and others reading your work. This message identifies what changes you made before adding your work to the stage, so you won't get lost with all the commits you made. Remember: The message has to be short, specific, and in the present tense).

---
## Workflow & Commands

After adding and committing your work using the two commands **`git add`** and **`git commit -m "short message"`**, you need to push all your work to the repository you just made (think of it as saving this screenshot permenantly on github!)   
However, before doing that, you need to build that bridge or connection between your git workspace and github (think of it as the Brooklyn Bridge that is built to connect Brooklyn with Manhattan, so people can transfer on it in New York!)
* To build that bridge, type git **`git remote add origin URL`**
    * 
* To push your work to github where you can save your work permenantly, type `git push -u origin master`

If you ever got lost, you can always type **`git status`** (optional)
* `git status` will show you if you haven't added your file once it was changed to the statging area which will appear in red.
* It will show you if you have added your file, but didn't commit yet which will appear in green.
* It will show you what commands you can use to fix your problems.
    * Example: If you haven't added your file to the stage, it will show you how you can add it by using `git add`

If you want to review your commits, you can head to github.com and look for that or you can type **`git log`** 
* `git log` will show you all the past commits made for this repository and will give you an SHA number for each commit (it is like an ID number for each commit).
* If your arrow got stuck in `git log`, press Q to quit.

---
## Rolling Back Changes