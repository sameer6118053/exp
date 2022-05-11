# Devops

Exp 1 
```
java -jar jenkins.war --httpPort=9191
```
```
class Test
{
    public static void main(String args[])
    {
        System.out.println("My name is "+args[0]);
        System.out.println("My surname is "+args[1]);
    }
}
```
```
Make Java file in a folder and copy its path
Then go to jenkins

Step 1 : New Item
Step 2 : Select Freestyle project
Step 3 : Add Build step : Execute Windows batch command

E:
cd E:\Devops\Exp
javac test1.java
java test1

Step 4 : Save and Build
```
Exp 2

```
1) hg (to check Mercurial is installed) / (hg config --edit) to change mercurial.ini

2) mkdir repo (in any drive C,D,E)

3) cd repo

4) hg init (for .hg file to be installed in repo)

5) hg clone http://www.selenic.com/repo/hello myHello (Cloning file from Mercurial)

6) cd myHello

7) (You can run miscelleneous such as hg summary, hg log etc)

8) Now go back to repo by (cd ..)

9) hg clone myHello myHelloClone (you make a directory clone of myHello)

10) Now manually (GUI) go to myHelloClone and access the Hello.c file and make some changes

11) go back to cmd and go to cd myHelloClone and type hg status

12) hg diff (To check the changes made in it)

13) hg commit -m "My first version" hello.c (to commit the changes made earlier in the hello.c file)

14) hg push ..\myHello

15) now go to myHello folder using cd..

16) hg update (to update the changes done in myHello folder)

17) Now manually (GUI) go and check the Hello.c file in myHello. You can see the changes that were done in myHelloClone/Hello.c in myHello/Hello.c
```
Exp 3 
```
1) Open Git Bash

2) mkdir DevOps

3) cd DevOps

4) git init

5) nano file1.txt

6) git add .

7) git commit -m "This is my first commit"

8) git status & git log (Miscellaneous commands)

9) git config --global user.name "Your username"

10) git config --global user.email "youremail@gmail.com"

11) Now to github.com on your desktop. Log in and create a new repository in your account.

12) Once done go to your new repository and copy the https link of your repository

13) Go back to Git bash and type
	git remote add origin https://github.com/....    <https link of your repository>

14) git push -u origin master

15) Now go back to gitub.com on your browser and check the master branch of your repository. You will see "file1.txt"  in it.
```
Exp 4
```
git config --global user.name "your_username"
git config --global user.email "your_email_address@example.com"
git init

##create doc file in local drive
git add .
git status
git commit - m "comment"
git push
git remote add origin url
git push --set-upstream origin master

##change to master branch in git hub repo and check if file is added
## add a new file 
git fetch
git merge 

## make another file 
git pull
git log

##to create a new branch
git checkout -b anybranchname
git checkout abovebranchname
git remote -v
git branch -vv
git ls -files

## to restore modified file, modify content of a file in local
git status
git restore filename
git status

git clone url
cd
```
Exp 5
```
1) sudo apt  update

2) sudo apt install -y docker.io (Hit Yes if a pop up comes once that command is executed)

3) sudo systemctl enable --now docker

4) sudo usermod -aG docker $USER

5) docker --version
```
Exp 6
```
1) nano Dockerfile (And write the below code in it and save)

FROM nginx:alpine
COPY . /usr/share/nginx/html

2) docker build -t html-server-image:v1 .

3) docker images (You can confirm that the above command has worked by running this command)

4) docker run -d -p 80:80 html-server-image:v1 (Run the following command to run the HTML container server)

5) Open browser and type "localhost:80"
```
