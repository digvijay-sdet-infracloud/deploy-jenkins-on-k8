# deploy-jenkins-on-k8

To deploy jenkins on k8, below configurations required

Pre-requisities:
1. Java
2. Kind/Minikube Cluster or Any Cloud Provider

Steps to Deploy Jenkins on K8
1. Create Namespace
2. Attach PV & PVC with storageclass and then mount the volume on pod/deployment
3. Create a Nodeport service

# Execute the jenkins service using below command 

4. kubectl -n jenkins port-forward service/<jenkins-service-name> 8080:8080
5. Launch http://localhost:8080

# To get the initialpassword of jenkins under jenkins home directory
6. k exec <pod-name> -n namespace -i -t -- bash <container-name>
7. cd /var/jenkins-home/secrets
8. cat initialPassword
