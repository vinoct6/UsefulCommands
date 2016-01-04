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
