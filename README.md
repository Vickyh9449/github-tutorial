# GitHub Tutorial

_by Vicky Huang_

---
## Git vs. GitHub
* Git: is a program in Github
  * Keeps snapshots of code 
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
6. After you have done that, switch over to your Cloud9 account and click on the gear icon located on the top right corner  
![Here's a screenshot](https://preview.c9users.io/vickyh9449/github-learning/fork-practice/Screen%20Shot%202016-10-24%20at%209.26.57%20PM.png)
7. Once you have clicked on the gear icon, go to "SSH Keys" and copy/paste your SSH key onto Github
   * It should start with `ssh-rsa`
8. After that, you would type in `ssh -T git@github.com`
   * The URL is suppose to have your Github username
9. After that, you have connected your Github account to your local repo, Cloud 9

---
## Repository Setup
To create a repository, there are a number of steps in completing this task.
1. You must log into your Cloud 9 and Github account and make sure the remote repo (Github) is connected to your local repo (Cloud 9)
   * If not, follow the steps to the Github setup as well as the SSH key setup
2. When you have completed step 1, go to Cloud 9 and make a new file
  * You would type in `mkdir file-name` and `cd file-name` to move into it
3. Next you would want to make a text file so you would type the syntax, `touch file text-name` to make a new text file
4. After that, bring your curser to the file you made and you would add any content you want to it. You could type anything and everything.
5. After doing so, go back down to your bash and now you would want to save those changes
6. If you want to save your changes, go to your Github account that should be signed in already.
7. Click on your profile icon and click "New repository"
8. After that, you would name the repository
   * **Make sure your directory name matches with the directory name in Cloud 9!! This is the most important part.**
   * After creating the new repository, there will appear two lines of code
9. After doing so, go back to your Cloud 9 and hover over to bash terminal (this is where you type all the code)
10. In bash, you would first add the file to save the changes, commit it with a message so that it's ready to be in the staging area, and finally pushing it to your remote repository which is Github
11. To do so, you would first type `git add text-name` 
12. Then `git commit -m "message to describe what changes/edits you made"` to take a screenshot of the code you have written
13. Finally go back to Github, copy and paste the two lines of code into the command line  
```
git remote add origin git@github.com:[username]/repo-name.git 
git push -u origin master
```



---
## Workflow & Commands
To have your repo running smoothly, you would need to make sure you are adding and commiting the files while making changes to the code. 
* To add a file, you would use `git add text-name`
  * This allows your changes in the files to be added in a snapshot
  * It gets ready to be saved and move the file onto the staging area
* To commit changes in a text file, you would use `git commit -m "message on what you edit"`
  * After adding your file, you would need a commit message to signify what you have edited
  * The commit message must be in present tense, short and descriptive
* To push changes from local repo (your computer) to remote repo (Github), you would use `git push`
* To check the condition of your file (to see if the file has been committed or not), you would use `git status`

---
## Collaboration
#### Forking
* Forking means making a copy of someone else's repo and saving it as their own remote repo
1. To fork a user's repo, you would need to log into your Github and Cloud 9 accounts
2. After that, go back to Github and go to [github.com/explore](https:/github.com/explore) to select a repo that you would like to fork
3. After choosing a repo, click on it and click on "fork" at the top right corner  
![Here is what to click on](https://preview.c9users.io/vickyh9449/github-learning/github-tutorial/Screen%20Shot%202016-10-28%20at%2012.23.26%20AM.png)
4. After forking, you would need to add it to you Cloud 9
5. To add it to ur Cloud 9, you would go to Github and click on the green button that says "Clone or Download"  
![This is how the button should look like](https://preview.c9users.io/vickyh9449/github-learning/github-tutorial/Screen%20Shot%202016-10-28%20at%2012.32.00%20AM.png)
6. After doing that, go back to Cloud 9 and go to your terminal
7. In your terminal, type in `git clone <URL>`
#### Cloning
* Cloning is basically copying a user's remote repo onto your local repo
* You can do this by selecting any repo you would like to clone, click on "Clone or Download", copy the link, and go back to Github
* In Github, you would go to your bash and type in `git clone <URL>`
#### Pull Requests
* A pull request is when you fork someone's repo, make changes, and want the owner of the repo to approve of your changes
* In order for them to see you changes, you need to submit a pull request
* This allows the owner to see what changes you would like to make on their repo
* In order to submit a pull request, the user must fork a repo and make changes to it before submitting a pull request
* After making changes to the forked repo on Cloud 9, the user would then have to go to their Github account and navigate to the forked repo
* After doing so, the user should find a button that says "New Pull Request" or "Create Pull Request"  
![Pull Request button](https://preview.c9users.io/vickyh9449/github-learning/github-tutorial/Screen%20Shot%202016-10-28%20at%2012.43.53%20AM.png)  
After clicking on the button, they would submit their pull request and wait for the owner of the repo to accept
#### Pull
* When an owner of a repo sees that they have pull requests, they can either accept them or deny them
* If they accept it, they would first have to merge the changes in order to have their new changes seen
* To merge pull requests, you would have to click on Pull Requests on the menu on the top of the screen
* After doing so, they would have to scroll down until they have found a green button that says "Merge Pull Request"
* When found, click on it and your changes and now ready to be pulled into your local repo or Cloud 9. 
* To see the changes on Cloud 9, you simply type in `git pull`
  *Make sure the files to your changes are opened
  * You can do this by going `cd` into it
---
## Screenshots
* When taking screenshots of code, it allows the viewers to visually see what you have done to be where you are now
* In order to make a screenshot, you must screenshot a part of code of anything from your computer
  * If you have a Mac, to screenshot, click on Command + Shift + 4
  * If you have a PC, use Snipping Tool that should be provided in your laptop
* After taking a screenshot, go to Cloud 9 and click on File on the top left corner and then click on "Upload local files"  
![Screenshot of menu bar](https://preview.c9users.io/vickyh9449/github-learning/github-tutorial/Screen%20Shot%202016-10-28%20at%2012.57.04%20AM.png)
* After that, uplaod your screenshot and you should see it show up on your file tree on the left
* When you see it, double click it so that it opens
* After doing so, go back to the top menu bar and click on "Preview"
* Under Preview, you should find an option that says "Raw Content of Screenshot..."  
![Screenshot](https://preview.c9users.io/vickyh9449/github-learning/github-tutorial/Screen%20Shot%202016-10-28%20at%201.00.48%20AM.png)
* When you see it, click on it and after that, click on the icon that's in the middle or next to "Browser"  
![Screenshot](https://preview.c9users.io/vickyh9449/github-learning/github-tutorial/Screen%20Shot%202016-10-28%20at%201.03.40%20AM.png)
* When you have clicked that, copy the link and use the template of adding an exclamation point first, then brackets to describe your screenshot, and parentheses to paste the URL you copied earlier
* After that, you have created your screenshot