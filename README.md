# Sample Java Application Instrumented with a New Relic APM Agent

This repository contains a simple Java application to calculate the nth number (between 1-90) in the Fibonacci sequence. It has no front end and runs locally in a terminal window. The built in load generator will generate and error every 4th attempt as it attempts to calculate a number outside of 1-90 on these attempts.

This application has been set up to be instrumented with New Relic APM. For similar versions of this same application, see the following repositories:

* [No Instrumentation](https://github.com/Bijesse/fibonacci-java-uninstrumented.git)
* [OTel for New Relic](https://github.com/Bijesse/fibonacci-java-otel) 

## Requirements
* A recent version of [Java](https://www.java.com/en/download/) and [Gradle](https://gradle.org/install/)  
* A free account with [New Relic](https://newrelic.com)

## To run this application with the New Relic Java agent

1. From a new terminal window, clone this repository to your local machine using Git `git clone https://github.com/Bijesse/fibonacci-java-apm`

2. Navigate into your new workspace using cd `fibonacci-java-apm`

3. Export your ingest license key:
```shell
export NEW_RELIC_LICENSE_KEY='your_license_key'
```
4. Build and run the app:
```shell
gradle bootRun
```
5. To generate traffic, run:
```shell
./load-generator.sh
```
6. Navigate to your New Relic account to see your data!