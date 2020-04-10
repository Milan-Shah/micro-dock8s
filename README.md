
# Microservices-Docker-K8s
This is a simple cloud application that I developed alongside the Udacity Cloud Engineering Nanodegree. It allows users to register and log into a web client, post photos to the feed, and process photos using an image filtering microservice. Following are the services involved in this project:

* “user” - allows users to register and log into a web client, 
* “feed” - allows users to post photos, and process photos using image filtering 
* “frontend” - acts as an interface between the user and the backend-services
* "reverseproxy" - For resolving multiple services running on same port in separate containers

Correspondingly, the project is split into following parts:
1. The RestAPI Feed Backend, a Node-Express feed microservice.
1. The RestAPI User Backend, a Node-Express user microservice.
1. The Simple Frontend - A basic Ionic client web application which consumes the RestAPI Backend.
1. Nginx as a reverse-proxy server, when different backend services are running on the same port, then a reverse proxy server directs client requests to the appropriate backend server and retrieves resources on behalf of the client.  


## Docker 
The application is divided the into smaller services for user, feed, frontend, reversproxy using Docker. 

## K8s 
I have created Kubernetes resources and deployed the application to Kubernetes cluster using kops + kubectl. I have also extended the application with deployments to be able to apply rolling-updates and rollbacks. 

## Travis CI
I have also integrated Travis CI for automating continuous integration (CI) and continuous delivery (CD).

## Screenshots
You can find the screenshots withing screenshots folder for below resources:
1. Udagram application running on localhost
1. Docker hub images
1. Running containers locally 
1. Travis-CI in action