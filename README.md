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












































































