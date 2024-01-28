# Reverse-Proxy-App
 
Reverse proxy application, using NGINX, Angular, MongoDB, SpringBoot.

## Required tools:

* Install Docker
* Install Minikube
* Install Kubernetes

## Deployment

* `minikube start` to start kubernetes cluster
```
 xxx@xxx-virtual-machine:~$ minikube start
 😄  minikube v1.32.0 on Ubuntu 22.04
 ✨  Using the docker driver based on existing profile
 👍  Starting control plane node minikube in cluster minikube
 🚜  Pulling base image ...
 🔄  Restarting existing docker container for "minikube" ...
 🐳  Preparing Kubernetes v1.28.3 on Docker 24.0.7 ...
 🔗  Configuring bridge CNI (Container Networking Interface) ...
 🔎  Verifying Kubernetes components...
     ▪ Using image gcr.io/k8s-minikube/storage-provisioner:v5
 🌟  Enabled addons: storage-provisioner, default-storageclass
 🏄  Done! kubectl is now configured to use "minikube" cluster and "default" namespace by default
```

* Deploy  `mongo` service using `mongo.yaml`
```
  kubectl create -f mongo.yaml 
```
* Deploy SpringBoot service using `backend.yaml`
```
  kubectl create -f backend.yaml
```
* Deploy Front End service using `front-end.yaml`
```
  kubectl create -f front-end.yaml
```
* Check the application
```
  minikube service frontend
```
  
## To find proper data go to /api/users

![image](https://github.com/xXvladosXx/Reverse-Proxy-App/assets/63474317/e176bde3-6b81-472f-9efe-65711f7502c1)

