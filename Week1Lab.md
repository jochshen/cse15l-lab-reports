# **Lab Report 1 - Remote Access and FileSystem (Week 1)**

## Let's Get Started! 

**Part 1 - Create CSE15L Account** 
1. Log into your account using [this](https://sdacs.ucsd.edu/~icc/index.php) link and your USCD account info.
2. Press on the button that starts with cs15l
![Image](buttonImage.png)
3. Press "Global Password Change Tool"
4. Press "Proceed to the Password Change Tool" 
5. Scroll down, and for username, enter the letters on the box in step 2 (should start with cs15l)
6. Sign in and they'll send an link to your school email to reset the password. 

**Part 2 - Visual Studio Code** 
1. Press [this](https://code.visualstudio.com/) link and follow the instructions to download Visual Studio Code 
2. After following the instructions, first window should look something like this 
![Image](vscode.png)
3. This is where you'll do most of you coding but for today, we'll just be linking your account 

**Part 3 - Remotely Connecting**
1. Press ```Command```(Mac) or ```Ctrl```(Windows) + ```Shift``` + ```P``` 
2. Type in: ```Terminal: Select Default Profile``` into the search bar 
3. Press ```bash``` profile 
4. Locate the terminal button on the top and press "New Terminal" 
![Image](terminal.png)
5. After pressing ``` Terminal ``` and  ``` New Terminal ```, a black box should pop up on the bottom 
![Image](terminalBox.png) 
5. To make sure you're on the right track, the right of the terminal should say ```bash```
![Image](bash.png)
6. In the terminal, type ```ssh <the username you put in Part 1 step 5>@ieng6.ucsd.edu```
7. Enter the password you made from Part 1 (you won't see anything so really focus and don't make typos :blush:)
After a couple seconds, you'll be prompted with a message that might look like 
```ssh cs15lsp23zz@ieng6.ucsd.edu The authenticity of host 'ieng6.ucsd.edu (128.54.70.227)' can't be established. RSA key fingerprint is SHA256:ksruYwhnYH+sySHnHAtLUHngrPEyZTDl/1x99wUQcec. Are you sure you want to continue connecting (yes/no/[fingerprint])?```
**Type yes**
8. You're screen should look something like this 
![Image](stats.png)
