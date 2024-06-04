# Deploy-with-nginx

- Add html page in /html directory
- Build docker image and push to docker hub
-     docker build -t ritish134/html-app:v1 .
-     docker push ritish134/html-app:v1

## Apply deployment.yaml file in k8s cluster
-     kubectl apply -f deployment.yaml
- Check if the pod is up and running
-     kubectl get pods
- Now to access the static web page by nginx container which is running inside the pod of k8s cluster
- Expose the deployment using k8s services
-     kubectl apply -f service.yaml
-     kubectl get svc
## Access the web page using IP address of the service with the particular port (here is mine)
  
  ![nginx](https://github.com/Ritish134/Deploy-with-nginx/assets/121374890/e52ec994-962b-47a4-bb99-0e80be911c15)


  ## Troubleshooting steps
  -     kubectl describe pods
