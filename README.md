# openshift-applications

This repository holds Spring Boot sample applications on OpenShift. It cover the basics of getting started with Spring Boot on OpenShift.

## Microservices Application
The microservice application is broken into three separate microservices and backing services:

* customers-service - maintains the customer information. On creating a customer it publishes a an event (command event) to create a payment account for the given customer.
* payment-account-service - maintains the payment account information. It consumes the event for creating a payment account for a customer and creates an account for a given customer.
* customer-composite-service - calls customers and payment account services to aggregate the customer and payment account information
* Demo database - Hold the tables for customer and account information.
* Kafka - A messaging broker 

The end-to-end architecture of the application is shown below.

## Deploying Application

## Pre-requisite
Before you try these examples download and setup [minishift](https://docs.openshift.org/latest/minishift/index.html)

## Start minishift
Start a minishift with no parameters
```
minishift start 
```

Start a minishift with 4GB memory and 2 CPUS and profile name called `springboot_msa_on_oc`
```
minishift --profile springboot_msa_on_oc --memory=4096 --cpus=2 start
```
## Common CLI commands
Get a list of PODs 
```
 oc get pods
```
Get a list of Services 
```
 oc get svc
```

## Deploying microservices and banking services

