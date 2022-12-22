Steps :

1. Start the Minikube - minikube start
2. Check Minikube status - minikube status
3. Allow Kubernetes to read our local Docker repository - eval $(minikube docker-env)
4. List all the Docker images - docker images
5. Navigate to project folder and create the image of the application
    docker build -t kubernetes-demo:1.0 .
6. Again check the list of Docker images - docker images
7. Create the K8S deployment file - deployment.yaml
8. Deploy the deployment file in the cluster with command : kubectl apply -f deployment.yaml
9. Check the deployment status : kubectl get depoyments
10. Check the running pods : kubectl get pods
11. Fetch the logs of running PODs : kubectl logs <POD Name>
12. Create a service.yaml for Service discovery, it will also act as a Load Balancer
13. Expose the app creating the service : kubectl apply -f service.yaml
14. Check the service status : kubectl get service
15. To get the URL type the command : minikube service kubernetes-demo-svc  --url
16. Application can be accessed by the URL retrieved at step 15
17. Dashboard can be launched using the command : minikube dashboard