kubectl apply -f nginx-custom-docker/frontend.yaml
kubectl port-forward service/frontend 8080:80
