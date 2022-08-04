# jenkin
maven jenkins
go to eclipse
Create a Maven Project - > File - > New -> Maven Project!
Select the quickstart archetype under org.apache.maven.archetypes and click on Next! select artifacts click on ok
Give Artifact ID of your choice and click Finish, Maven Project is created!
In the created project, Check for App.java file containing Hello World program!
Right click on your project and Run As Maven Clean - It clears out the existing classes that you compiled from last compile!
Check the console for Build Success!
Right click on your project and Run As Maven Install - to add artifact(s) to the local repository!
Check the console for Build Success!
Right click on your project and Run As Maven Install - use to specify test classes or methods we want to execute!
Click on Run!
Now Run the Project as Java Application to test the output!
Select the Created project from the list - > Click Ok!
In the console we can view the output of the project!
Next is to push the project into GitHub, for this, create a new repository in GitHub!
Next is to push the project into GitHub, for this, create a new repository in GitHub!
Click on create repository!
Copy the HTTPs URL as shown to be copied into Jenkins!
Open Git Bash to push the project into GitHub![image](https://user-images.githubusercontent.com/101937605/182816082-2bce5a13-dc6c-4e5e-b141-06fde6e1f68b.png)
copy the eclipse file make into working directory by git init
now copy the http code by 
$ git remote add origin http code https://github.com/archanareddyse/mavenweb.git
$ git remote -v
$ git push origin -u main
now refresh by the github we see all will be uploaded here
open jenkins -> freestyle project-> scm paste the url of git -> main
first configure the jenkins by java and maven
add the plugins by 
maven integration
build pipeline
pipeline utility
copy articats
deploy to cintainer these are must for maven project
in maven Follow the same goals as done in eclipse starting with clean and install![
Now in post build actions-> select Archive the artifacts, to send the output of build project to the testing team!
If we want to archive all the artifacts type **/* as shown!
Now the next step is to build other projects, where we will create a test project which will be triggered by the build project!
Ignore the red warning, as we have not yet created the test project!
Create a new freestyle project test as shown and click ok!
To forward the artifacts of the previous project to the current test project, select copy the artifacts from another project in Build as shown!
Give the name of the project from which we want to copy the artifacts and check the box ->stable build only->to copy all the artifacts type **/*!
Now select Invoke top-level Maven targets in build!
This time give the goal as test after selecting the Maven version!
In post-build actions->select Archive the artifacts!
To save all the artifacts->type **/* and Apply->Save!
Create a pipeline by clicking on + symbol in the dashboard ->a pipeline is a collection of events or jobs which are interlinked with one another in a sequence!
Give a name to the pipeline->select Build Pipeline View->create!
Select the first project to trigger the execution->build project!
Click on Run -> click on the small black box to open the console to check if the build is success!





