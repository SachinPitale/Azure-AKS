# YAML Basics

## Step-01: Comments & Key Value Pairs
- Space after colon is mandatory to differentiate key and value
```yml
# Defining simple key value pairs
name: Kubernetes
Language: yaml 
```

## Step-02: Dictionary / Map
- Set of properties grouped together after an item
- Equal amount of blank space required for all the items under a dictionary
```yml
technology :
  name: Kubernetes
  Used: IT
  Language: yaml 
```

## Step-03: Array / Lists
- Dash indicates an element of an array
```yml
technology :
  name: Kubernetes
  Used: IT
  Language: yaml 
  Component: # List  
    - Pod
    - Replicaset
  Cloud: [EKS, AKS]   # List with a differnt notation  
```  

## Step-04: Multiple Lists
- Dash indicates an element of an array
```yml
technology :
  name: Kubernetes
  Used: IT
  Language: yaml 
  Component: # List  
    - Pod
    - Replicaset
  Cloud: [EKS, AKS]   # List with a differnt notation  
  features: # 
    - name: Deployment
      description: Pod
    - name: Service
      description: Loadbalancer           
```  


## Step-05: Sample Pod Tempalte for Reference
```yml
apiVersion: v1 # String
kind: Pod  # String
metadata: # Dictionary
  name: myapp-pod
  labels: # Dictionary 
    app: myapp         
spec:
  containers: # List
    - name: myapp
      image: sachinpitale22/mynginx_image1:v1-release
      ports:
        - containerPort: 80
          protocol: "TCP"
        - containerPort: 81
          protocol: "TCP"
```




