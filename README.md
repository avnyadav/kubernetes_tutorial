
Get the status of nodes in kubernetes cluster
```
kubectl get nodes
```

Output:
```
NAME       STATUS   ROLES           AGE     VERSION
minikube   Ready    control-plane   8m16s   v1.24.1
```


List pod
```
kubectl get pod
```
List services
```
kubectl get services
```
Output:
```
NAME         TYPE        CLUSTER-IP   EXTERNAL-IP   PORT(S)   AGE  
kubernetes   ClusterIP   10.96.0.1    <none>        443/TCP   9m40s
```


Help for creating kubectl component
```
kubectl create -h
```
Check the output
[Kubectl create -h](kubectl_create_help.md)


Create deployment nginx
```
kubectl create deployment ngnix-depl --image=nginx
```

```
kubectl get deployment
```

Edit the deploymnet 
```
kubectl edit deployment ngnix-depl
```


### Debug kubectl pod


```
kubectl logs pod_id
```
Let's deploy mongodb deploy

```
kubectl create deployment mongo-depl --image=mongo
```


if pod has not yet started use below command to check the status
```
kubectl describe pod POD_NAME
```
mongo-depl-85dcbc595b-6mnl7


open container terminal
```
 kubectl exec -it mongo-depl-85dcbc595b-6mnl7 -- bin/bash
```

Delete the deployment
```
kubectl delete deployment name
```

Create deployment using yaml file
```
kubectl apply -f [filename]


To check ip mapping
```
kubectl describe service [service_name]
```

```
kubectl get pod -o wide
```


get status of configuration