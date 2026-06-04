# JavaMicroservices

## Reference - https://javatechonline.com/microservices-architecture-in-java/

# Monolithic -

## here we put everything at one place 

## here all features or we can say modules of a project  are in single application 

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

## Lets say we have some changes in rewards feature can i independently deploy rewards feature ? NO

## In case of Monolithic Architecture all the other features will be deployed again with rewards

# i.e we need to deploy entire Application when there is a change in single module/feature also

# What are Microservices (MS) -

##  The term Microservices was first introduced by Martin Fowler and used at a software architects’ workshop in 2011 for the first time. 

##  Few organizations such as Netflix, Amazon are currently using microservices.

Let Suppose we have Yono SBI Application Backend 

It has various features like rewards,creditcard,fundtransfer,nps ,account balance etc 

In Case of Microservice Architecture all features will be in a separate application

Eg There will be a diffrerent Microservice for rewards , creditcard,fundtransfer,nps ,account balance etc 

# Each Microservice has its own DB 

# Independent Deployment 

# Easy to scale applications 

# All Features  of project  are independently created 

# Different Technologies i.e one MS can be build on nodejs one on java etc 

## Each MS will have its own deployment pipeline and infrastructure 

## If a  credit card service wants to send data to  rewards service how it is possible in Microservices ?

### Bcz in Monolithic Architecture only a simple function call is needed 

### In case of  Microservices we need to manage interservice communication also

## There are 2 types of interservice communication 

### a) Synchronous b) ASynchronous

# a) Synchronous

In case of Synchronous communication a simple http or https call is made between the two Microservices ( eg between credit card and rewards)
i.e using resttemplate , restclient, feignclient etc 

# b) ASynchronous

Event Driven or Producer Consumer Model
One MS will send message to Message Broker then message broker to another MS

## Famous Message Brokers are RABBITMQ and apache KAFKA 

## When to use Microservices (MS) ?

### In case of large enterprise applications like banking applications eg yono sbi we can use 

### Lets say if rewards ms fails the credit card service will still run because it is independent

# Typical System Design 

Client -> Edge -> Application Layer -> DB -> Observability

# In  edge layer 

-  DNS will get resolved i.e url will be resolved
-  Then we have CDN for region specific content delivery
-  Then we have load balancer
-  Then API Gateway i.e it routes request to MS
  
# DB
Do learn Database System Design Concepts like Database Replication , Database Sharding , Database Partioning 

# Observability
It includes logging and monitoring

## Use cache to reduce hits to DB 





