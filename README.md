# Git Command Practice
# List Of Git Cmd With Example

Some Of Important Git Command With Example Asked In Interview.

Good luck for your interview 😊

---

### Table of Contents

| No. | Git Command |
|---- | ---------
|1  | [git init](#git-init) |
|2  | [git add](#git-add) |
|3  | [git commit](#git-commit) |
|4  | [git status](#git-status) |
|5  | [git config](#git-config) |

Note : For all git Cmd you need to install git on your local machine.

1. ### git init

   This command turns directory inti a empty git repository
 
      ```git
      iMac-Pro-2 git-command-practice $   mkdir git-command-practice 
      iMac-Pro-2 git-command-practice $   cd git-command-practice 
      iMac-Pro-2 git-command-practice $   git init
      ```

2. ### git add

   Add files to the staging for git
 
      1. **git add . : add all file to the staging of git.**
      ```git
      iMac-Pro-2 git-command-practice $   touch file1.js 
      iMac-Pro-2 git-command-practice $   touch file2.js 
      iMac-Pro-2 git-command-practice $   touch file3.js 
      iMac-Pro-2 git-command-practice $   git add .
      ```

      2. **git add <filename> : add specified file to the staging of git.**
      ```git
      iMac-Pro-2 git-command-practice $   touch file4.js 
      iMac-Pro-2 git-command-practice $   touch file5.js 
      iMac-Pro-2 git-command-practice $   git add file4.js
      ```

      3. **git add <filename1> <filename3> <filename3>  : add multiple specified file to the staging of git.**
      ```git
      iMac-Pro-2 git-command-practice $   touch file6.js 
      iMac-Pro-2 git-command-practice $   touch file7.js 
      iMac-Pro-2 git-command-practice $   touch file8.js 
      iMac-Pro-2 git-command-practice $   git add file6.js file7.js file8.js 
      ```


3. ### git commit

   Records the changes made to the file in local repository. 
   Each commit has a unique ID.
 
 
   first Do some changes in some created files then.

      1. **git commit <file1> <file2> -m "<commit_message>" : commit only spacified file.**

      ```git
      iMac-Pro-2 git-command-practice $   git commit file1 file2 -m "First Commit"
      ```

      2. **git commit  -m "<commit_message>" : commit all file that we modified and execute git add cmd.**
       
      For this if we added some file already, and modified it then we need to execute git add . or git add <file1> <file2> 
      ```git
      iMac-Pro-2 git-command-practice $   git commit  -m "first commit"
      ```


4. ### git status


   This cmd returns the current state of the repository.
   It return current branch name, modified files, untracked files and more information.
   If there is no changes it'll return `nothing to commit, working directory clean`. 
 
 
      ```git
      iMac-Pro-2 git-command-practice $   git status


      On branch master
      Your branch is up to date with 'origin/master'.

      Changes not staged for commit:
      (use "git add <file>..." to update what will be committed)
      (use "git restore <file>..." to discard changes in working directory)
	   modified:   README.md

      Untracked files:
      (use "git add <file>..." to include in what will be committed)
	   file.js

      ```


5. ### git config


   with GIT, There are many configrations and settings possible.
   `git config` is how to assign this settings. 
   Two important settings are user.name and user.email.  
 
      1. **Set Global Username and Email in git config.**

      ```git
      iMac-Pro-2 git-command-practice $   git config --global user.name "AcousticKrishna"
      iMac-Pro-2 git-command-practice $   git config --global user.email "acoustickrishna@gmail.com"
      ```

      2. **Set In Current Repository Username and Email in git config.**

      ```git
      iMac-Pro-2 git-command-practice $   git config user.name "AcousticKrishna"
      iMac-Pro-2 git-command-practice $   git config user.email "acoustickrishna@gmail.com"
      ```
     
   

**[⬆ Back to Top](#table-of-contents)**

