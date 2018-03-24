# openshift-applications

This repository holds Spring Boot sample applications on OpenShift. It cover the basics of getting started with Spring Boot on OpenShift covering the following,

* Deploy and Debug Spring Boot Application in Openshit

## Pre-requisite
Before you try these examples download and setup [minishift](https://docs.openshift.org/latest/minishift/index.html)

## Start minishift
```
minishift start 
```
Start a minishift with no parameters

```
minishift --profile springboot_msa_on_oc --memory=4096 --cpus=2 start
```
Start a minishift with 4GB memory and 2 CPUS and profile name called `springboot_msa_on_oc`

## Common commands

```
 ./mvnw fabric8:deploy 
 ./mvnw fabric8:undeploy 
 ./mvnw fabric8:resource 
```

* build and deploy the maven project to OpenShift
* undeploy the maven project if it exits in OpenShift
* Generate the OpenShift manifests

