maven
=====

activities on maven 


this information provides the details of 

            1. what is maven plugin?
            2. what is the use of maven plugin?
            3. configuration of maven plugin?
            4. generating archetype from maven central repository?
            5. creation of our own archetype?
            
            
            
            MAVEN
            
            as all of know maven is a build tool that hepls you in building a project step by step & it downloads the all neccessary dependencies 
            at the time building the project.
            
            instead of checking requirements manually, we enterd the all list of dependencies & plugins in a file called pom.xml which is main 
            root folder of the project.
            
            
            INSTALLATION AND CONFIGURATION OF MAVEN PACKAGE
            
            installation and configuring of maven plugin is different from windows,linux here i am providing in linux environment
            type: apt-get install mvn <enter>
            
            check with: mvn --version
            mvn repository path: home/<rootuser>/.m2/repositories/
            
            
            
            GENERATING MAVEN ARCHETYPE
            
            maven archetype is template from central repository/local repository that gives you skelton of the project.
            As need of your project needs you can select the archetype
              1. type: mvn archetype:generate
              it will prompt you the archetype number for console entry.
            
              
              2. enter the number based on description.
              it will prompt you for groupId
            
              
              3. groupId is like package details of maven project.
              like test.mvn.project
              path test->mvn->project
              
              
              4. artifactId
              projectId details or root directory of a project.
              ex: myApp
              
              
              5. version
              version is the version of your project release.
             
             
             project path will be: test/mvn/project/myApp/
             
             Here myApp is the root folder for the entire project and skelten inside the myApp depends on the archetype.
             
             
            CREATION OF OUR OWN ARCHETYPE
            
            1. create empty project with your own skelton and pom.xml
            2. pom.xml file should consists all neccessary plugins (regards to your project) & maven-archetype-plugin
            3. copy your redily project into root folder. (myApp)
               like my files consists which i copied
                      myApp/src/main/java/myApp.java
                      myApp/src/test/java/myApp.java
               make sure groupId & artifactId should not have any mistakes
            4. type: mvn archetype:create-from-project
            5. you can check some files in target folder
               target->generated-soureces->archetype
            6. entered into above mentioned path and type:mvn clean install
            7. now go and check in .m2/repositories/ 
            
                    you should have  test/mvn/project folders with some project files
                    you can find some jar files
                    in .m2.archetype-metadata.xml file updated with your groupId&artifactId
                    now add the local archetype into the eclipse.
            
            
            
          
