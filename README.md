# deployment-kubernates-object

COMMANDS USED IN THIS VIDEO

sudo su

command to install docker is

sudo apt update && apt -y install docker.io

install Kubectl now with the given link

curl -LO https://storage.googleapis.com/kubern... -s https://storage.googleapis.com/kubern... && chmod +x ./kubectl && sudo mv ./kubectl /usr/local/bin/kubectl

install Minikube with the given link

curl -Lo minikube https://storage.googleapis.com/miniku... && chmod +x minikube && sudo mv minikube /usr/local/bin/

apt install conntrack

minikube start --vm-driver=none
minikube status
kubectl version
kubectl get nodes

******************************

kind: Deployment
apiVersion: apps/v1
metadata:
   name: mydeployments
spec:
   replicas: 2
   selector:     
    matchLabels:
     name: deployment
   template:
     metadata:
       name: testpod
       labels:
         name: deployment
     spec:
      containers:
        - name: c00
          image: ubuntu
          command: ["/bin/bash", "-c", "while true; do echo Technical-Guftgu; sleep 5; done"]


********************************************END*********************
