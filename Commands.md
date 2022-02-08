
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
kubectl get pods --show-labels
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
### If pod have two or more containers
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
### Add new label to running pod
```bash
kubectl label pods <your-pod-name> <labelKey>=<labelValue>
```
### Add multiple new label to running pod
```bash
kubectl label pods <your-pod-name> {key1=value1,key2=value2,key3=value3}
```
### Edit label of the runing pod without stoping it
```bash
kubectl label pod <podName> --overwrite <labelKey>=<LabelValue> 
```
### Delete label of the runing pod without stoping it
```bash
kubectl label pods <your-pod-name> <label-name>- 
```
>*end minus(-)sign is important*

