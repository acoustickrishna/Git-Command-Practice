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
|6  | [git branch](#git-branch) |
|7  | [git branch <branch_name>](#git-branch-<branch_name>) |
|8  | [git checkout <branch_name>](#git-checkout-<branch_name>) |
|9  | [git merge <branch_name>](#git-merge-<branch_name>) |
|10 | [git branch -d <branch_name>](#git-branch--d-<branch_name>) |
|11 | [git branch -D <branch_name>](#git-branch--D-<branch_name>) |
|12 | [git checkout -b <branch_name>](#git-checkout--b-<branch_name>) |
|13 | [git clone <ssh-url>](#git-clone-<ssh-url>) |
|14 | [git pull origin <branchname>](#git-pull-origin-master) |
|15 | [git stash save "<msz>"](#git-stash-save-"<msz>") |
|16 | [git stash list](#git-stash-list) |
|17 | [git stash apply <stashid>](#git-stash-apply-<stashid>) |
|18 | [git stash pop](#git-stash-pop) |
|19 | [git log](#git-log) |
|20 | [git revert](#git-revert) |



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


6. ### git branch


  This cmd show the list of branch 
 
      ```git
      iMac-Pro-2 git-command-practice $   git branch
      ```
      Above cmd will show 

      ```git
      * master
      ```
      Here * denotes your current branch you are working on.


7. ### git branch <branch_name>

  This cmd will create a new branch but you still on the old branch.
 
      ```git
      iMac-Pro-2 git-command-practice $   git branch features
      ```
      Above cmd will show 

      ```git
      features
      * master
      test1
      ```
      Here * denotes your current branch you are working on.


8. ### git checkout <branch_name>

  This cmd will switch to specified branch.
 
      ```git
      iMac-Pro-2 git-command-practice $   git checkout features
      ```
      Above cmd will show 

      ```git
      * features
      master
      test1
      ```
      Here * denotes your current branch you are working on.


9. ### git merge <branch_name>

  This will Join two or more development histories together.
 
  Lets create a scenario we have 2 branch `master` and `features` 
  we have a file name is `file1.js` and contain some code on `master branch` is follow.

      ```
      console.log("Some Console log data");

      ```

  now we checkout on `features branch` and do some changes as follow 

      ```
      console.log("Some Console log data");
      console.log("this is some changes");
      ```   

  save it then `commit` it on `features branch` 
  then `checkout` on `master branch`

  now We execute `git merge features` 
  then the code inside features branch will be available inside master branch 

  finally execute `git push origin master` to show code on origin branch 

      ```git
      iMac-Pro-2 git-command-practice $   git merge features
      ```
      
    



10. ### git branch -d <branch_name>

  This cmd will delete branch here -d will not delete unmerge changes if there.
  its a safe delete. 
 
      ```git
      iMac-Pro-2 git-command-practice $   git branch -d features
      ```
      Above cmd will show 

      ```git
     Deleted branch features (was c717736).
      ```

11. ### git branch -D <branch_name>

  This cmd will delete branch here -d will delete unmerge changes if there.
  its a not safe delete. 
 
      ```git
      iMac-Pro-2 git-command-practice $   git branch -D features
      ```
      Above cmd will show 

      ```git
     Deleted branch features (was c717736).
      ```

12. ### git checkout -b <branch_name>

  This cmd will create a new branch and also switch on new branch.
 
      ```git
      iMac-Pro-2 git-command-practice $   git checkout -b features
      ```
      Above cmd will show 

      ```git
      * features
      master
      test1
      ```
      Here * denotes your current branch you are working on.

13. ### git clone <ssh-url>

  it will clone the remote repository to the local
 
      ```git
      iMac-Pro-2 git-command-practice $   git clone git@github.com:acoustickrishna/Git-Command-Practice.git
      ```

14. ### git pull origin master

  This cmd will pull the changes from specified branch to local branch
 
      ```git
      iMac-Pro-2 git-command-practice $   git pull origin master 
      ```

15. ### git stash save "<msz>"

  To save changes made when they are not in state to commit them to the repository

  lets Assume the latest commit was already done
  start working on the next patch, and discovered I was missing something
  then we can do this save our work to continuee in future

      ```git
      iMac-Pro-2 git-command-practice $   git stash save "work on other task for live"
      ```

      This cmd will show following result on terminal
      ```git
      Saved working directory and index state On master:work on other task for live
      ```

16. ### git stash list

  it will list all the saved stash 
      ```git
      iMac-Pro-2 git-command-practice $   git stash list
      ```

      This cmd will show following result on terminal
      ```git
      stash@{0}: On master: work on other task for live
      stash@{1}: On master: work on other task for live2
      ```

17. ### git stash apply <stashid>

  it will use to apply a stash by stashid but it never remove the stash, it will be available inside stash list.
      ```git
      iMac-Pro-2 git-command-practice $   git stash apply stash@{0}
      ```


18. ### git stash pop

  it will use to apply a stash using the method of pop, it never the stash, after run `git stash pop` stash not avaliable inside stash list or stash will dropped.

      ```git
      iMac-Pro-2 git-command-practice $   git stash pop
      ```

      After run this cmd it will show this result

      ```
      On branch master
      Your branch is up to date with 'origin/master'.

      Changes to be committed:
      (use "git restore --staged <file>..." to unstage)
            new file:   file10.js

      Changes not staged for commit:
      (use "git add/rm <file>..." to update what will be committed)
      (use "git restore <file>..." to discard changes in working directory)
            modified:   README.md
            deleted:    file1.js

      Dropped refs/stash@{0} (ce89a53f2a110e780ee723240ff6b393ace732ba)
      ```



19. ### git log


  The Git Log tool allows you to view information about previous commits that have occurred in a project.

  In other world it will use to get all commit history.


      ```git
      iMac-Pro-2 git-command-practice $   git log
      ```
  After run this cmd we will get output like this.

      ```
            commit 2051047776ce6d1794b80be31584cb7a431fe81a (HEAD -> master, origin/master)
            Author: indianic <indianic@indianics-iMac-Pro-2.local>
            Date:   Fri May 7 16:15:29 2021 +0530

            git merge

            commit 15ed46aae320428f597a1a88eba0d8f34c8000fd (origin/test2branch)
            Author: indianic <indianic@indianics-iMac-Pro-2.local>
            Date:   Fri May 7 15:57:37 2021 +0530

            some changes

            commit a148cc5750fb4e4660d3ad82b0ccf5efd67ec63e
            Author: indianic <indianic@indianics-iMac-Pro-2.local>
            Date:   Fri May 7 15:53:54 2021 +0530

            some chnages
      ```

      some more log CMD

      ```git
      iMac-Pro-2 git-command-practice $   git log --all
      ```
      You can force the log tool display all commits (regardless of the branch checked out) by using the –all option.


      ```git
      iMac-Pro-2 git-command-practice $   git log -2 
      ```
      this cmd will show last 2 log


      ```git
      iMac-Pro-2 git-command-practice $   git log --author "krishna"
      ```
      this cmd will show by author name    
      

      ```git
      iMac-Pro-2 git-command-practice $   git log --after "2014-02-01" 
      ```
      this cmd will show by log after date
  

      ```git
      iMac-Pro-2 git-command-practice $   git log --before "2014-02-02"
      ```
      this cmd will show by log before date


      ```git
      iMac-Pro-2 git-command-practice $   git log --after "2014-02-01" --before "2014-02-02"
      ```
      this cmd will show by log before date and after date


      ```git
      iMac-Pro-2 git-command-practice $   git log --oneline
      ```
      this cmd will View Just One Line Per Commit


       ```git
      iMac-Pro-2 git-command-practice $   git log --pretty=format:"Commit Hash: %H, Author: %aN, Date: %aD"
      ```
      Format the Git Log Output



20. ### git revert

  In Git, the term revert is used to revert some changes. The git revert command is used to apply revert operation. It is an undo type command. However, it is not a traditional undo alternative. It does not delete any data in this process; instead, it will create a new change with the opposite effect and thereby undo the specified commit. Generally, git revert is a commit.
  
      ```git
      iMac-Pro-2 git-command-practice $   git stash apply stash@{0}
      ```


**[⬆ Back to Top](#table-of-contents)**