# ReplicaSets with YAML

## Step-01: Create ReplicaSet Definition
- **replicaset-definition.yml**

## Step-02: Create ReplicaSet
- Create ReplicaSet with 3 Replicas
```
# Create ReplicaSet
kubectl apply -f 01-replicaset-definition.yml

# List Replicasets
kubectl get rs
```
- Delete a pod
- ReplicaSet immediately creates the pod. 
```
# List Pods
kubectl get pods

# Delete Pod
kubectl delete pod <Pod-Name>
```

## Step-03: Create LoadBalancer Service for ReplicaSet

- **Create LoadBalancer Service for ReplicaSet & Test**
```
# Create LoadBalancer Service
kubectl apply -f 02-replicaset-LoadBalancer-servie.yml

# List LoadBalancer Service
kubectl get svc

# Access Application
http://<Load-Balancer-Service-IP>

```

## API References
- [ReplicaSet](https://kubernetes.io/docs/reference/generated/kubernetes-api/v1.19/#replicaset-v1-apps)