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

Then, You are done with your initial setup

---
## Repository Setup



---
## Workflow & Commands



---
## Rolling Back Changes