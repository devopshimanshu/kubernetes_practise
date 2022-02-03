
# Kubernetes Commands

All commands that we had practised are listed over here.

    


## Pods
Comands related to pod are listed below 
### Create a pod using file
```bash
kubectl create -f <podFileName>
kubectl apply -f <podFileName>
```
### Check pod is running or not with little details
```bash
kubectl get pods 
kubectl get pods -o wide
```
### Get details of the pod
```bash
kubectl describe <podName>
```
### Check logs of the pod
```bash
kubectl logs <podName>
```
### Get inside pods container
```bash
kubectl exec -it <podName> --./bin/bash
```
### Run command in a container without entring into it
```bash
kubectl exec <podName> <command which we need to execute>
example
    kubectl exec nginx-pod env
```
### if pod have two or more containers
```bash
kubectl exec -it <podName>  -c <conatinerName> --./bin/bash
```
### Expose pod to external world
```bash
kubectl expose pod <podName> --port=<portNumber> --type=LoadBalancer
```
### Expose pod to external world
```bash
kubectl expose pod <podName> --port=<portNumber> --type=LoadBalancer
```
### Delete pod
```bash
kubectl delete pod <podName>
```

## Service
### Get details of the services
```bash
kubectl get services
kubectl get services -w
```
### Delete a services
```bash
kubectl delete services
```