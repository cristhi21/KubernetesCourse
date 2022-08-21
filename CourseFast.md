# Curso Fast K8S

```sh
# Version K8S
kubectl version --client --output=yaml

# start local cluster
minikube start

# show dashboard
minikube dashboard

# show status
minikube status

# Create pod:
kubectl run webserver1 --image=nginx

# Show pods
kubectl get pods
kubectl describe pods

Podemos revisar el Dashboard luego de crear el pod


# Access a pod by proxy
kubectl proxy
127.0.0.1:8001
127.0.0.1:8001/version
curl http://127.0.0.1:8001/version

http://127.0.0.1:8001/api/v1/namespaces/default/pods/webserver1/
http://127.0.0.1:8001/api/v1/namespaces/default/pods/webserver1/proxy/


# Commons Commands kubectl
kubectl get pods
kubectl describe pods
kubectl logs webserver1
kubectl exec <name_pod> <command_run_within_pod>
kubectl exec webserver1 ls|bash


# Create and post services
kubectl get deployment
kubectl describe deployments

kubectl get pods
kubectl get services

kubectl describe service



# Scale services
# Escalando el deployment escalamos los pods
kubectl scale deployment/nginx1
kubectl get pods -o wide
```