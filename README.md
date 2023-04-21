# Software-Installation

**Minikube Installation**
```
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube_latest_amd64.deb
sudo dpkg -i minikube_latest_amd64.deb
```
**Start minikube cluster**
```
minikube start --force
```
**Pause and Stop the minikube Cluster**
```
minikube pause
minikube stop
```
**Install kubectl on Ubuntu**
```
sudo apt-get update
sudo apt-get install -y ca-certificates curl
sudo apt-get install -y apt-transport-https
sudo curl -fsSLo /etc/apt/keyrings/kubernetes-archive-keyring.gpg https://packages.cloud.google.com/apt/doc/apt-key.gpg
echo "deb [signed-by=/etc/apt/keyrings/kubernetes-archive-keyring.gpg] https://apt.kubernetes.io/ kubernetes-xenial main" | sudo tee /etc/apt/sources.list.d/kubernetes.list
```
```
sudo apt-get update
sudo apt-get install -y kubectl
```
**Kubectl version**
```
kubectl version --client
```
**Interact with your cluster**
```
kubectl get po -A
```
**Use kubectl to forward the port command**
```
kubectl port-forward service/hello-minikube 7080:8080
```
Your application is now available at 
```
http://localhost:7080/
```
**Browse the catalog of easily installed Kubernetes services**
```
minikube addons list
```
**Enable the Ingress controller**
1: To enable the NGINX Ingress controller, run the following command:
```
minikube addons enable ingress
```
2: Verify that the NGINX Ingress controller is running
```
kubectl get pods -n ingress-nginx
```
**Delete all of the minikube clusters**
```
minikube delete --all
```
**Minikube Dashboard URL**
```
minikube dashboard --url
```




