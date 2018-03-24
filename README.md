# openshift-applications

This repository holds Spring Boot sample applications on OpenShift. It cover the basics of getting started with Spring Boot on OpenShift covering the following,

* Deploy and Debug Spring Boot Application in Openshit

## Pre-requisite
Before you try these examples download and setup https://docs.openshift.org/latest/minishift/index.html[minishift]

## Start minishift
----
minishift start <1>
----
<1> Start a minishift with no parameters

----
minishift --profile springboot_msa_on_oc --memory=4096 --cpus=2 start <2>
----
<2> Start a minishift with 4GB memory and 2 CPUS and profile name called `springboot_msa_on_oc`

## Common commands
[source,sh]
----
 ./mvnw fabric8:deploy <1>
 ./mvnw fabric8:undeploy <2>
 ./mvnw fabric8:resource <3>
---- 

<1> build and deploy the maven project to OpenShift
<2> undeploy the maven project if it exits in OpenShift
<3> Generate the OpenShift manifests

