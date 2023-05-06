# Maven_examples

Maven is open source developed by Apache org

Maven developed using java

Maven used to perform build automation for java projects

Maven called as java build tool

archetype represent what type of project is

Maven providing 1500+ archetype

Ex. maven-archetype-quickstart: java standalone app

    maven-archetype-webapp: java web app


## Create Java Package on Windows 11 using Maven


### Pre-requisite:


**1) Install Java**

Download java from oracle site : "https://www.oracle.com/sg/java/technologies/javase/javase8-archive-downloads.html"

Install jdk-8u202-windows-x64.exe

set below system environment variables:

Home: JAVA_HOME = c:\program files\java\jdk.8.0_202

Path: path = c:\program files\java\jdk.8.0_202\bin

Verify java installation using command $ java -version


**2) Install Maven**

Download apache maven 3.9.1 from apache site : "https://maven.apache.org/download.cgi"
Extract file "apache-maven-3.8.5-bin.zip" to the folder "c:\program files" 

Set system environment variables:

Home: MAVEN_HOME = c:\program files\apache-maven-3.9.1-bin\apache-maven-3.9.1

path: path = c:\program files\apache-maven-3.9.1-bin\apache-maven-3.9.1\bin

Verify java installation using command $ mvn -version


### Example 1 : Create Application Package

1. Create "Maven_Practice" folder on the D drive

2. Open Powershell and change Directory to the folder "Maven_Practice" 

3. Run below command to create blank java project 

```
$ mvn archetype:generate "-DgroupId=com.javan.dev" "-DartifactId=MyMavenApp01" "-DarchetypeArtifactId=maven-archetype-quickstart" "-DinteractiveMode=false"
```

  If command run succesfully then Check "MyMavenApp01" folder got created and Verify "src" folder & "pom.xml" file present in it

4. Compile java code 

```
$ mvn compile 
```

  If command run succesfully then Verify "target" folder folder present inside "MyMavenApp01" along with "src"

5. Test the code (optional)

```
$ mvn test 
```

  Verify command run succesfully and there are no errors

6. Create Package

```
$ mvn package 
```

  If command run succesfully then Verify jar file got created in the target folder, you can use this jar package to deploy on the web server 


### Example 2 : Create WebApp Package

1. Create "Maven_Practice" folder on the D drive

2. Open Powershell and change Directory to the folder "Maven_Practice" 

3. Run below command to create blank java project 

```
$ mvn archetype:generate "-DgroupId=com.javan.dev" "-DartifactId=MyWebApp01" "-DarchetypeArtifactId=maven-archetype-webapp" "-DinteractiveMode=false"
```

  If command run succesfully then Check "MyWebApp01" folder got created and Verify "src" folder & "pom.xml" file present in it

4. Compile java code 

```
$ mvn compile 
```

  If command run succesfully then Verify "target" folder folder present inside "MyMavenApp01" along with "src"

5. Test the code (optional)

```
$ mvn test 
```

  Verify command run succesfully and there are no errors

6. Create Package

```
$ mvn package 
```

  If command run succesfully then Verify jar file got created in the target folder, you can use this jar package to deploy on the web server 


