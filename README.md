# TstNG_Ob_AP
# TestNG_Ob_AppPercy
Basic repo for a manual languag binding (exsting TestNG BrowserStack integration) with Observability and App Percy


# testng-appium-app-browserstack

This repository demonstrates how to run Appium tests in [TestNG](http://testng.org) on BrowserStack App Automate.

![BrowserStack Logo](https://d98b8t1nnulk5.cloudfront.net/production/images/layout/logo-header.png?1469004780)

## Setup

### Requirements

1. Java 8+

    - If Java is not installed, follow these instructions:
        - For Windows, download latest java version from [here](https://java.com/en/download/) and run the installer executable
        - For Mac and Linux, run `java -version` to see what java version is pre-installed. If you want a different version download from [here](https://java.com/en/download/)

2. Maven
   - If Maven is not downloaded, download it from [here](https://maven.apache.org/download.cgi)
   - For installation, follow the instructions [here](https://maven.apache.org/install.html)

### Install the dependencies

To install the dependencies for Android tests, run :
```sh
cd android/testng-examples
mvn clean
```


## Getting Started with only Observability

Getting Started with Appium tests in TestNg on BrowserStack couldn't be easier!

### **Run first test :**

- Observability integration also shared here:  https://www.browserstack.com/docs/test-observability/quick-start/testng
- Please follow the steps:
- Add SDK dependency to pom file: 
```
         <dependency>
            <groupId>com.browserstack</groupId>
            <artifactId>browserstack-java-sdk</artifactId>
            <version>LATEST</version>
            <scope>compile</scope>
        </dependency>
        
```
- Create and add browserstack.yml to contain following values:
```
userName: USERNAME
accessKey: ACCESSKEY
buildName: "Your static build/job name of CI goes here"
projectName: "Your static project name goes here"
framework: testng
browserstackAutomation: **false**
testObservability: true
```
- Run first test by using the command:  mvn test -P first
- Check the dashboard at Observability Dashbaord (https://observability.browserstack.com/)
------------------------------------------------------------------------------------------------
## Getting Started with only Observability and App Percy

Getting Started with Appium tests in TestNg on BrowserStack couldn't be easier!

### **Run first test :**

- Observability integration also shared here:  https://www.browserstack.com/docs/test-observability/quick-start/testng
- Please follow the steps:
- Add SDK dependency to pom file:
- For Observability add BrowserStack SDK 
```
         <dependency>
            <groupId>com.browserstack</groupId>
            <artifactId>browserstack-java-sdk</artifactId>
            <version>LATEST</version>
            <scope>compile</scope>
        </dependency>
        
```
- For App Percy follow the steps - https://docs.percy.io/v2-app/docs/appium-for-java-1

- Create and add browserstack.yml to contain following values:
```
userName: USERNAME
accessKey: ACCESSKEY
buildName: "Your static build/job name of CI goes here"
projectName: "Your static project name goes here"
framework: testng
browserstackAutomation: **false**
testObservability: true
```
- Run first test by using the command:  npx percy app:exec -- mvn test -P first
- Check the dashboard at Observability Dashbaord (https://observability.browserstack.com/)
- Check the Percy runs at Percy dashboard 
