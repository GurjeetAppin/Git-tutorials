Git Commands :-
1. git --version :- To check the version of git.
2. git status :- To check the status.
3. git init :- Convert the repository to git repository.
4. git add . :- This command is make a stage for files.( To add the code on git first you make a stage and after that to commet the code. )
5. git commit -m "version 1" :- To commet the code into the git. 
                            Syntax :- git commit -m "your message".
6. git log :- To check the work of developers.
7. git config --global user.name "Gurjeet Developer" :- To change the name that saved in git that use this command. ( --global :- this keywords use for all the repository for changing the name or email id. If you not add this --global keyword that are valid only where you work on repository. )
8. git config --global user.email "gurjeet@appin.com" :- To change the email id that saved in the git that used this command.

<!-- How to set the remote origine and what is meaning of remote origane -->

Origin :- Origin mean koi asa remote origin koi ase website koi asa server jo hamare code ko save kare. Aur wahe se koi dusra banda pull karde.

When you create a repository after this line select the ssh. after this line 
Quick setup — if you’ve done this kind of thing before. and If you are using the gitbash. 
And copy the line :- git remote add origin git@github.com:GurjeetAppin/Git-tutorials.git
This command is created according to your repository when you are created.

If you are using the other like gitlab. Then you copy the this line 
git@github.com:GurjeetAppin/Git-tutorials.git. That are avaliable after the HTTPS/SSH.

Add origin command :- git remote add origin git@github.com:GurjeetAppin/Git-tutorials.git
Push origin command :-  git branch -M main
                        git push -u origin main

Set a SSH :-
If you are created a new account then you set your SSH key in your Github account.
1. Goto the your prfile setting >> SSH and GPG key >> select the generating SSH key >> Select the Generating a new SSH key and adding it to the ssh-agent

2. Check your email that are use in github. For check the email using git command :- git config user.email. 
Copy this email and add this in this command :- ssh-keygen -t ed25519 -C "140533763+gurjeetappin0208@users.noreply.github.com"

3. Goto the :- Adding your SSH key to the ssh-agent section.
 3.1 :- Copy this command :- eval "$(ssh-agent -s)"
 3.2 :- Copy this command :- ssh-add ~/.ssh/id_ed25519

4. Goto the :- Add the SSH public key to your account on GitHub. For more information, see "Adding a new SSH key to your GitHub account." and click it.
5. Copy the SSH public key to your clipboard.
    command :- clip < ~/.ssh/id_ed25519.pub
    5.1 :- Click in url bar and press the ctrl+v and copy the key
    Key :- ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIBl5pVFqidlR5+2LVd8e/Y7KdznPA4K8rZuGUjw42TS5 140533763+gurjeetappin0208@users.noreply.github.com

<!-- After that you will push your code into the github account. -->
Push command :- git push -u origin main
<!-- After that you change in the file and push the code -->
1. Check the status using command :- git status
2. Make a stage using command :- git add .
3. Commit the code using command :- git commit -m "your comments"
4. Push the code into the github using command :- git push -u origin main
<!-- If you change the code into the github this changes also reflect when you pull the code form github -->
Pull command :- git pull origin main

<!-- How to check the differnce between two files. -->
1. git diff filename.extension :- This command used for differnce between two files.
2. git status
3. git add .
4. git commit -m "your message"

If you are see the differnce of stage file. Then you used the this command.
1. Syntax :- git diff --staged filename.extension 
             git diff --staged utils.txt

<!-- To rewert the code before commit -->
1. git reset utils.txt :- First you unstaged the file using this command
2. git status :- To check the status.
3. git checkout utils.txt :- This command rewert the code.
If anyone is changed the multiple files. Then we rewert the code using this command
4. git checkout .

<!-- Type of staging -->
1. git add -A :- Stages all 
2. git add . :- Stages new and modified, without deleted. If you are add new and modified code and not delete anything. Jo bhi delete ho chuka hoga woh stage nahi hogi baki ka sara work jo ha woh stage ho jaye ga.
3. git add -u :- yeh command stage kara ge modified or delete files ko. Ja kar apne ko new file bani hai yeh use stage nahi kare ga.

<!-- Cloning the code -->
1. ls -la :- this command is showing the files and folder inside the project.
2. git clone git@github.com:GurjeetAppin/Git-tutorials.git :- This command is clone the prject from then github. These are steps are perform to clone the repository into local system.
    2.1 Make a folder in your directory 
        Example :- this is a folder name :- Git clone repo
    2.2 Open the Git clone repo and run the git bash
    2.3 Goto the github and click on Clone or Download button and select the SSH based url.
    2.4 git clone git@github.com:GurjeetAppin/Git-tutorials.git :- run this command.
    2.5 git clone git@github.com:GurjeetAppin/Git-tutorials.git . :- If you want to download same as folder name then you paste the url with this command and after this add a dot then the code is download same as its with same name.
 
<!-- If you want to ignore the files in github  -->
1. touch .gitignore :- This command is make a new file the name is .gitignore.
2. li -la :- Showing the all files that are avaliable inside the local repository.
3. notepad .gitignore :- This command is open the file inside the notepad.Type in this file like that.
4. code .gitignore :- This is command is open the file inside the visual studio code.
    For example :- utils.txt :- this is a file name.
                   *.pyc :- this is a python based file.
                   *.sql :- this is a sql based file.
4. git rm --cached filename :- If you are alread track a file and you don't want to track this file use this command.
But at the end it's depends on you what are you want to ignoring. So first you analized what you want to ignore and after that create a ignore code.

<!-- Branches  -->
If you want to copied the project and make a new branch in github and work on this copied that is called branch.
-->> First you want to create a repository in the github after that you copied the repository and upload the code into new branch <<--
Using a bit bash use this command for branches.
1. git branch :- This command showing the list of branch.
2. git branch branchname :- This command is make a copy of branch. Example :- git branch login-system.
3. git checkout login-system :- This command used for switched on branch to another branch.
4. git branch :- To check the branch is switched.
5. git status :- To check branch used the login system.
6. git add . :- Make a staging of file.
7. git commit -m "your message". :- To commit the code.
8. git push origin yourBranchName :- To push the code in new branch that created. Example :- git push origin login-system.

<!-- To merge the code in main branch -->
1. git branch :- To check the list of branches.
2. git checkout mainBranchName :- Switched to the main branch.
3. git merge nameYourCopiedBranchName :- To merge the code using this command. Example :- git merge login-system
4. git push -u origin main :- To push the code in main branch.

<!-- Deleted the branch -->
1. git branch -D yourCopiedBranchName :-  To delete the branch from local system.Example :- git branch -d login-system.
2. git push origin --delete login-system :- This command delete the branch from github.
