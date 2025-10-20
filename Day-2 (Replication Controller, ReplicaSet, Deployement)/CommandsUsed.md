# Kubernetes Commands

## 1. **Replicaset Management**
- **Create Replicaset**  
  `kubectl apply -f nginx-replicaset(Task-2).yaml`
  
- **Scale Replicaset**  
  `kubectl scale replicaset nginx-replicaset --replicas=6`

- **Delete Replicaset**  
  `kubectl delete replicaset nginx-replicaset`

## 2. **Deployments and Pods**
- **Get Deployments**  
  `kubectl get deployments`
  
- **Get Pods by Label**  
  `kubectl get pods -l app=v1`
  
- **Set Image for Deployment**  
  `kubectl set image deployment/nginx nginx=nginx:1.23.4`

- **Check Rollout Status**  
  `kubectl rollout status deployment/nginx`

- **Get Pods with Wide Output**  
  `kubectl get pods -l app=v1 -o wide`

- **Describe Pod**  
  `kubectl describe pod <pod-name>`

- **Scale Deployment**  
  `kubectl scale deployment nginx --replicas=5`

## 3. **Rollout and Revision Management**
- **View Rollout History**  
  `kubectl rollout history deployment nginx`
  
- **Undo Rollout to Specific Revision**  
  `kubectl rollout undo deployment/nginx --to-revision=1`
