# 1. Deploy-a-Java-Application-on-Jenkins

## 2. Create an EC2 instance 

![1](https://github.com/adrydry/Deploy-a-Java-Application-on-Jenkins/assets/102819001/d88a4b06-8cb0-417b-bd63-bdd3e55d6da9)

## 3. Install Jenkins

- Install Java

![1](https://github.com/adrydry/Deploy-a-Java-Application-on-Jenkins/assets/102819001/8b05350d-e635-45fa-a4cd-0f1ac1d4565c)

- Install Jenkins

![1](https://github.com/adrydry/Deploy-a-Java-Application-on-Jenkins/assets/102819001/7f1a4570-d25f-4d01-854d-45b0b2051b91)

- Execute the java war file
java -jar jenkins.war

![1](https://github.com/adrydry/Deploy-a-Java-Application-on-Jenkins/assets/102819001/8a3bac02-92e9-4111-ae63-fb19c07940f8)

- Change the default port of Jenkins

Because, many applications or software can run at the same time on the default port 8080 of Jenkins, we will affect another port number to our Jenkins server:8082 
java -jar jenkins.war --httpPort=8082

## 4. Access Jenkins from the browser with the port 8082

![1](https://github.com/adrydry/Deploy-a-Java-Application-on-Jenkins/assets/102819001/afeb70f2-07a1-4430-909f-5542b234a9a5)

## 5. Insert Administrator password to the jenkins server

Paste the token number or cat /root/.jenkins/secrets/initialAdminPassword

![1](https://github.com/adrydry/Deploy-a-Java-Application-on-Jenkins/assets/102819001/7c1d2e17-3717-4f61-aab7-d5772328725f)

 ## 6. Install Suggested Plugins
Install Suggested Plugins instead of Select Plugins to install because Jenkins by himself know which plugins are necessary for him.

## 7. Create First Admin User

We create our Admin account is Jenkins is ready for use

![1](https://github.com/adrydry/Deploy-a-Java-Application-on-Jenkins/assets/102819001/5b1dc41f-d693-46d8-abcf-b19d4b7602d3)

## 8. Setting features in the Jenkins Server

To easily integrate Jenkins with another tools, inside the Jenkins Server, go to **Manage Jenkins**.

- **Manage Plugins**: Allow us to download different plugin of the technologies that we want to configure with Jenkins 
For this project, we will install **JDK**: Eclipse Temurin Installer and OpenJDK native plugins , **OWASP**: Owasp dependency check plugins, **Docker**: Docker, Docker pipeline, Docker build step, cloudbees Docker build and publish; **Sonarqube**: sonarqube scanner.

- **Global configuration** allow us to configure all the plugins, we just downloaded to our jenkins server.

**Configure JDK**
Under JDK installation, Click on Add JDK and define the version of Java, we want to use for our pipeline

![1](https://github.com/adrydry/Deploy-a-Java-Application-on-Jenkins/assets/102819001/5d73aebc-e9ec-4bd3-ab42-10833e5cb371)

**Configure Maven**

We just need to provide the version of Maven, we will use inside our pipeline.(Refer to the version downloaded on our EC2)

![1](https://github.com/adrydry/Deploy-a-Java-Application-on-Jenkins/assets/102819001/084c18f2-3135-4e67-b1df-d34e207c6621)

**Configure Dependency-check(OWASP)**

![1](https://github.com/adrydry/Deploy-a-Java-Application-on-Jenkins/assets/102819001/8afb0ce3-bea3-4606-bd2d-af7c5e0eb2bd)

**Configure Docker**

![1](https://github.com/adrydry/Deploy-a-Java-Application-on-Jenkins/assets/102819001/15ef9ee9-fc59-4304-843c-e3e612d0a9bb)

Save all the changes

- **Configure system**
Is the place where we configure differents servers (Nexxus server, Sonarqube server,...) with Jenkins. There are many ways to do that but the more secure way is to go to Configure System.

- **Manage nodes and cloud**

Is the location where we can see which nodes/ VM/ Slaves will be used to run your project

-**Configure Global Security**

This is the security location of the jenkins server

-**Credentials**
We add credential

Let's create our Job. 

1- **Create a freestyle job**

This is used to perform small task like building and generate an artifact. In this case, we don't have to write many code

Specify the git repository of the code, the credentials and select Invoke top-level Maven targets with the goals clean compile and clean package

2- **Pipeline job**



## 9. Install Tomcat

Our Tomcat server is up and running

![1](https://github.com/adrydry/Deploy-a-Java-Application-on-Jenkins/assets/102819001/f5fd34c0-82ef-42a2-9e14-642cee3273e2)







































