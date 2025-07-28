kubectl apply -f configmap.yaml
kubectl apply -f deployment.yaml
kubectl port-forward service/configmap-frontend 8080:80
