# GitHub Tutorial

_by Vicky Huang_

---
## Git vs. GitHub
* Git: is a program in Github
  * Keeps snapshots of the code 
  * Does not require Github
  * Runs on Command Line
* Github: is a program that has Git in it
  * Stores code in a cloud
  * Requires Git
  * Tracks changes in code visually
  * Is a website (github.com)
  * Basic workflow

The difference between Git and Github is Git takes snapshots of code and does need Github while on the other hand, Github requires Git and stores code in a "cloud".


---
## Initial Setup
##### **Github Setup**
1. To set up a Github account, you would need to go to (www.github.com)
2. Next, you would need to click on Sign up
3. After clicking "Sign up", you would type in your information
4. When done, the email you used to set up the account, go to it and verify your email
   * If not, Github would suspect you to be a robot and you would have to verify your humanity  
##### **SSH Key**
1. To set up the SSH key, you would need to login to your Github account
2. Next, on the top right corner, click on your icon
3. After clicking on your icon, click on "Settings" 
4. When you are in the settings, go to "SSH and GPG Keys"  
![Here's a screenshot](https://preview.c9users.io/vickyh9449/github-learning/fork-practice/Screen%20Shot%202016-10-24%20at%208.30.44%20AM.png?_c9_id=livepreview0&_c9_host=https://ide.c9.io)
5. Next click on new "SSH key" and name it "cloud9"
   * Make sure it's all lower case, the program is case sensitive
6. After you have done that, switch over to your Cloud9 account and click at the gear icon on the top right corner  
![Here's a screenshot](https://preview.c9users.io/vickyh9449/github-learning/fork-practice/Screen%20Shot%202016-10-24%20at%209.26.57%20PM.png)
7. Once you have clicked on the gear icon, got to "SSH Keys" and copy/paste your SSH key onto Github
   * It should start with "ssh-rsa"
8. After that, you would type in `ssh -T git@github.com`
   * The URL is supposed to have your Github username
9. After that, you have connected your Github account to ur local repo, Cloud 9

---
## Repository Setup
To create a repository, there are a number of steps in completing this task.
1. You must log into your Cloud 9 and Github account and make sure the remote repo (Github) is connected to your local repo (Cloud 9)
   * If not, follow the steps to the Github setup as well as the SSH key setup
2. When you have completed step 1, go to Cloud 9 and make a new file
  * You would type in `mkdir file-name` and cd into it
3. Next you would want to make a text file so you would type the syntax, `touch file text-name` to make the text file
4. After that, bring your curser to the file you made and you would add any content you want to it. You could type anything and everything.
5. After doing so, go back down to your bash and now you would want to save those changes
6. If you want to save your changes, go to your Github account that should be signed in already.
7. Click on your profile icon and click "New repository"
8. After that, you would name the repository
   * Make sure your directory name mathces with the directory name in Cloud 9!! This is the most important part.
9. After doing so, go back to your Cloud 9 and hover over to bash terminal (this is where you type all the code)
10. In bash, you would first add the file to save the changes, commit it with a message so that it's ready to be in the staging area, and finally pushing it to your remote repository which is Github
11. To do so, you would first type `git add text-name" 
12. Then `git commit -m "message to describe what changes/edits you made"`
13. Finally `git push` to push the changes to Github



---
## Workflow & Commands