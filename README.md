# UsefulCommands
Useful commands

######Maven Quick start java project
mvn archetype:generate -DgroupId={project-packaging} 
   -DartifactId={project-name} 
   -DarchetypeArtifactId=maven-archetype-quickstart 
   -DinteractiveMode=false
   
#####Clear (MERGE_HEAD exists) in git
rm -rf .git/MERGE*


##### Grep commands

grep -i "java.home" server.log  //Case insensitive search

ls  | grep -r "GroupRegression" .   (search for a string in the current directly recursively and list all the files)

ls | grep -i "java.home" serve* (search all files starting with the name server)

grep -w "is"  (search for whole word instead of substring)

grep -v "go" demo_text  (Invert Match)

grep -c "java.home" server.log (count all matches)

grep -cv "java.home" server.log (how many lines do not match the pattern ? )

grep -l "java.home" *  (search all files and list files that matches this pattern) 

grep -n "java.home" * (show line number of the match)


##### Check running java processes

jps

##### Set current time in linux
date -s "6 JAN 2016 02:11:00"


##### Git commands

git config --list  (list all the configuration)

Also for specific keys :

git config user.name 

$ git status -s   (short status)
MM FirstFile.txt  (staged and modified)
 M "another file.txt"  (modified)
A  rose.txt  (untracked file is staged)
?? jasmine.txt (untracked)

##### Ignoring files :
Add patterns to .gitignore file your root directory.


$ cat .gitignore
*.[ox]   [Don't track files ending with .o or .x ]

git log --oneline

git log --pretty=format:"%h %ad - %s [%an]"
08467cf Wed Jan 13 13:33:59 2016 +0530 - third aero change [=]

%ad - author date
%an - author name
%h hash
%s subject
%d ref names

.git/info/exclude    - use this for local ignore

git blame <file name>


git reset HEAD^  (unstage the recent commit and move it to parent of the current head)
 
git reset --hard HEAD^     (HEAD^ means parent of the current head)

git checkout -- fileName  <last comitted version)

git commit --amend -a -m "adding product"  (amend previous commit)

##### Rebasing

When you have a master branch and an admin branch, to rebase
go to admin branch and  git rebase master
Then go to master and do  git merge admin

##### Interactive Rebase
git rebase -i HEAD~3











