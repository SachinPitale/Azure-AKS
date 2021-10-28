# PODs with YAML
## Step-01: Kubernetes YAML Top level Objects

- **01-kube-base-definition.yml**
```yml
apiVersion:
kind:
metadata:
  
spec:
```
-  [Pod API Objects Reference](https://kubernetes.io/docs/reference/generated/kubernetes-api/v1.19/#pod-v1-core)


- **Create Pod**
```
# Create Pod
kubectl create -f 02-pod-definition.yml
[or]
kubectl apply -f 02-pod-definition.yml

# List Pods
kubectl get pods
```


- **Create LoadBalancer Service for Pod**
```
# Create Service
kubectl apply -f 03-pod-LoadBalancer-service.yml

# List Service
kubectl get svc

# Access Application
http://<Load-Balancer-Service-IP>

```

## API Object References
- [Kubernetes API Spec](https://kubernetes.io/docs/reference/generated/kubernetes-api/v1.19/)
- [Pod Spec](https://kubernetes.io/docs/reference/generated/kubernetes-api/v1.19/#pod-v1-core)
- [Service Spec](https://kubernetes.io/docs/reference/generated/kubernetes-api/v1.19/#service-v1-core)


