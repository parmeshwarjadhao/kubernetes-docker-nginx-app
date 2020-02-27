# k8s-docker-nginx-static-html-demo

## Must read

Here is a quick [link](https://medium.com/containermind/a-beginners-guide-to-kubernetes-7e8ca56420b6) that explains the various aspects within kubernetes.

Other useful links:

- https://kubernetes.io/docs/concepts/
- 


## Prerequisites 

- docker installed 
- kubernetes installed

## System Configuration at time of test 

- macOS Mojave - Version: 10.14.5 
- Docker Desktop - Version 2.0.0.3 (31259)
- Kubernetes  - Version: 1.10.11

## Build Image

To build the docker image run the following command on the terminal:
`docker build -t kubernetes-docker-nginx-static-html-demo:v1 .`

To list the created docker images run the command on the terminal:
`docker images`

![docker-nginx-static-html-demo-docker-list-image](images/docker-nginx-static-html-demo-docker-list-image.png?raw=true "Terminal Docker List Images Screenshot")

## Run the Docker Container

Run the following command to spin up the container server:
`docker run -d -p 45678:80 nginx-static-html-image:v1`

To list all the containers running run this command on the terminal:
`docker ps -a`

![docker-nginx-static-html-demo-list-container-image](images/docker-nginx-static-html-demo-list-container-image.png?raw=true "Terminal Docker List Containers Screenshot")

## Test

Run the following command to ensure the server is running:
`curl localhost:45678`

You can also view it in the browser by going to `localhost:45678` and the HTML page similar the the one below will show up:

![docker-nginx-static-html-demo-browser-image](images/docker-nginx-static-html-demo-browser-image.png?raw=true "Browser Screenshot")


# Cleanup

To stop the container that is running use this command 
`docker stop {container_id}`

To delete the container that was created use this command
`docker rm {container_id}`

To delete the docker image that was created 
`docker rmi {image_id}`

![docker-nginx-static-html-demo-cleanup-image](images/docker-nginx-static-html-demo-cleanup-image.png?raw=true "Terminal Docker Cleanup Screenshot")
