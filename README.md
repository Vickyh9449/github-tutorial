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
  * Is a website [github.com](https://github.com/)
  * Basic workflow
  * Allows developers to collaborate easily

The difference between Git and Github is Git takes snapshots of code and does require Github. While on the other hand, Github requires Git and stores code in a "cloud".


---
## Initial Setup
##### **Github Setup**
1. To set up a Github account, you would need to go to [www.github.com](www.github.com)
2. Next, you would need to click on the "Sign up" button
3. After clicking "Sign up", you would need to type in your information. You should be using your hstat email and the username and password should be the same one you use for your hstat email.
4. When done, go to the email you used to set up the account and verify your email
   * If not, Github would suspect you to be a robot and you would have to verify your humanity  
##### **SSH Key**
1. To set up the SSH key, you would need to login to your Github account
2. Next, on the top right corner, click on your profile icon
3. After clicking on your profile icon, click on "Settings" 
4. When you are in the settings, go to "SSH and GPG Keys"  
![Here's a screenshot](https://preview.c9users.io/vickyh9449/github-learning/fork-practice/Screen%20Shot%202016-10-24%20at%208.30.44%20AM.png?_c9_id=livepreview0&_c9_host=https://ide.c9.io)
5. Next click on new "SSH key" and name it "cloud9"
   * Make sure it's all lower case, the program is case sensitive
6. After you have done that, switch over to your Cloud9 account and click at the gear icon on the top right corner  
![Here's a screenshot](https://preview.c9users.io/vickyh9449/github-learning/fork-practice/Screen%20Shot%202016-10-24%20at%209.26.57%20PM.png)
7. Once you have clicked on the gear icon, go to "SSH Keys" and copy/paste your SSH key onto Github
   * It should start with `ssh-rsa`
8. After that, you would type in `ssh -T git@github.com`
   * The URL is supposed to have your Github username
9. After that, you have connected your Github account to your local repo, Cloud 9

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
To have your repo running smmothly, you would need to make sure you are adding or commiting files while checking to see if they have been committed. 
* To add a file, you would use `git add text-name`
  * This allows your changes in the files to be added in a snapshots
  * It gets ready to be saved and move onto the staging area
* To commit changes in a text file, you would use `git commit -m "message on what you edit"`
  * After adding your file, you would need a commit message to signify what you have edited
  * The commit message must be in present tense
* To push changes from local repo to remote repo, you would use `git push`
* To check the condition of your file (to see if it has been committed or not), you would use `git status`