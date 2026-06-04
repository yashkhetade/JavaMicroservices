# JavaMicroservices

## Reference - https://javatechonline.com/microservices-architecture-in-java/

# Monolithic -

## here we put everything at one place 

## here all features are in single application 

## It is a single unified system where all features are build and deployed together

### Let Suppose we have Yono 2.0 Application Backend 

###  It has various features like rewards,creditcard,fundtransfer,nps ,account balance etc 

###  In Case of Monolithic Architecture all features will be in a single application 

# Benefits of Monolithic Architecture

1) Simple to develop 

2) Easy to test 

3) Easy to deploy. We just need to copy the packaged application(jar, war, etc.) to a server.

4) Simple to scale (We can perform horizontal scaling by running multiple instances behind a load balancer)

5) # Here CodeBase is big 

# Drawbacks of Monolithic Architecture

1) Even for a small change in the code, entire application needs to be re-built and re-deploy.

2) Hence, one small problem may affect the entire application.

3) Adding new concept/technologies/new Integration may become very complex. 

4) As the number of modules increase, then application size increases, downtime for re-deployment may also increase accordingly.


## It is difficult to scale  Monolithic Application 

## Lets suppose we have created sbi yono application backend and deployed it on aws env

## If more request and user are visting the fund transfer feature then i need to scale entire application rather than a single feature rewards

## But due to Monolithic Architecture unneccesary we need to scale rewards , credit cards and other features to

## What are Microservices (MS) -

# The term Microservices was first introduced by Martin Fowler and used at a software architects’ workshop in 2011 for the first time. 

##  Few organizations such as Netflix, Amazon are currently using microservices.

Let Suppose we have Yono SBI Application Backend 

It has various features like rewards,creditcard,fundtransfer,nps ,account balance etc 

In Case of Microservice Architecture all features will be in a separate application

Eg There will be a diffrerent Microservice for rewards , creditcard,fundtransfer,nps ,account balance etc 

# Each Microservice has its own DB 

# Independent Deployment 

# Different Technologies i.e one MS can be build on nodejs one on java etc 




