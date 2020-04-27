# multi-k8s
![system](https://github.com/hwdavr/multi-k8s/blob/master/system_archict.png)

## Create PGPASSWORD 
Create a password for the postgress and service.  
```
kubectl create secret generic pgpassword --from-literal PGPASSWORD=12345asdf
```

## Install Ingress-nginx 
Deploy Ingress-nginx based on your platform from: https://kubernetes.github.io/ingress-nginx/deploy/    


## Build and Run 
```
# Install cert-manager
kubectl apply -f https://raw.githubusercontent.com/jetstack/cert-manager/release-0.6/deploy/manifests/00-crds.yaml
# Deploy all
kubectl apply -f k8s
```

## Visit the Web App 
Check host and IP address by using `kubectl get ingress`. 
Add the following line to the bottom of the /etc/hosts file. 
```
192.168.XXX.XXX    k8s-multi.com,www.k8s-multi.com
```
Now you can use browser to visit "k8s-multi.com" or "www.k8s-multi.com".  

