
## Cd into the solution directory
```
cd K8S_Lab_solution
```

## Apply K8s objects
```
kubectl apply -f .
```

## Set vote namespace in the context
```
kubectl config set-context --current --namespace=vote
```

## Create secrets from env file
```
kubectl create secret generic psql-secrets --from-env-file=psql_secrets -n vote
```

## Continuously watch pods
```
watch -n 0.5 kubectl get pods
```

## Get the service IP
```
minikube service --all -n vote
```

## Remove all objects
```
kubectl delete -f .
kubectl delete secret psql-secrets
```