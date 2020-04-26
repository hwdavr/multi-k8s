# multi-k8s

## Create PGPASSWORD 
```
kubectl create secret generic pgpassword --from-literal PGPASSWORD=12345asdf
```

## Install Ingress-nginx 
Deploy Ingress-nginx based on your platform from: https://kubernetes.github.io/ingress-nginx/deploy/.  


## Build and Run 
```
# Install cert-manager
kubectl apply -f https://raw.githubusercontent.com/jetstack/cert-manager/release-0.6/deploy/manifests/00-crds.yaml
# Deploy all
kubectl apply -f k8s
```

