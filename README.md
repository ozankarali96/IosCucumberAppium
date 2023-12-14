# Trendyol Appium-Java Ios Case



## General info
It is written in Java and Appium framework. This project is written in accordance with the Page object pattern structure and supports BDD along with Cucumber. Logging was done with log4j to see the progress of the project infrastructure and find errors.
When Cucumber scenarios failed or were successful, screenshots were taken and attached to the report. In this way, it is easier to solve the error with a screenshot of the step in which the error occurred.
If you want to use another device-driver, you can set it directly from the config.properties file without entering the code.
## Technology
* [Java](http://java.com)
* [Cucumber](https://cucumber.io)
* [Appium](https://appium.io/docs/en/2.1/)
* [Log4j](https://logging.apache.org/log4j/2.x/)
* POM
* XCode
* XCode Simulator

## Execution assistance
After pulling the project to your local:
```sh
mvn clean install
```
command will trigger the already written testRunner class.
Test Runner is currently set up to run all tests.
```java
@CucumberOptions(
        features = "src/test/resources/features/",
        plugin = {
                "pretty",
                "html:Reports/cucumber-pretty.html",
                "json:Reports/CucumberTestReport.json",
                "junit:Reports/CucumberTestReport.xml"
        }
```
The feature file given from here can be run. In addition, by adding the tags parameter, your tag-based tests can be grouped and run.