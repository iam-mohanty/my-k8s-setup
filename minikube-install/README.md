# my-minikube-setup

1. create one ubuntu ec2 instance
2. t2.medium
3. k8s-key.pem
4. ssh,all traffic ( anywhere )
5. launch instance
6. now connect , instance

## 1. Update ubuntu package file and install docker

sudo apt update -y

sudo apt install docker.io -y

## 2. Now install minikube package and istallation file

curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64 

sudo install minikube-linux-amd64 /usr/local/bin/minikube && rm minikube-linux-amd64

## 3. Now check minikube version

minikube version

## 4. apply Docker permission to all user

sudo usermod -aG docker $USER && newgrp docker

## 5. Now start minikube service

minikube start --driver=docker

## 6. Now install kubectl 

sudo snap install kubectl --classic

## 7.  now check cluster

kubectl get nodes

..........................................END.............................................................................
