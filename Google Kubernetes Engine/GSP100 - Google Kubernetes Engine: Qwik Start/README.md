This directory contains instructions and Kubernetes deployment configuration for the "Google Kubernetes Engine: Qwik Start" lab.

## Lab Steps

### 1. Set default compute region and zone

```bash
gcloud config set compute/region us-west1
gcloud config set compute/zone us-west1-a
```
### 2. Create a GKE cluster
```
gcloud container clusters create --machine-type=e2-medium --zone=us-west1-a lab-cluster
```
### 3. Get authentication credentials
```
gcloud container clusters get-credentials lab-cluster
```
### 4. Deploy hello-server app
```
kubectl create deployment hello-server --image=gcr.io/google-samples/hello-app:1.0
kubectl expose deployment hello-server --type=LoadBalancer --port 8080
```
### 5. View service
```
kubectl get service
# Then access: http://[EXTERNAL-IP]:8080
```
### 6. Delete the cluster
```
gcloud container clusters delete lab-cluster
```
