# This file contains details of the files and contents of the files

we will be using "eksctl create cluster --config-file=eks.yaml"

This will start creating the EKS cluster once the EKS cluster is provisioned we can use below commands to list the nodes

kubectl get nodes # This will display nodes in the cluster

K8s Resouorces:
Namespaces is a isolated project space where you can create resources related to your project

Pod: Pod is a smallest deployable unit in Kubernetes
pod vs container
---
Pod contains multiple containers
containers inside pod share same n/w and storage

kubectl apply -f pod.yaml
kubectl get pods # to view available pods
kubectl describe pod nginx

Multicontainer deployment
We can deploy multiple container into a pod
after multiple pods are deployed into a container we can use below command to enter into one of the pod.
"kubectl exec -it multicontainer -c almalnx -- bash"
"kubectl exec -it multicontainer -c nginx -- bash"

Kubernetes nodes run on ephemeral storage similar to containers meaning temporary based on the traffic.

