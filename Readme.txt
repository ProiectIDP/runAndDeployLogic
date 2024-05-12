The docker compose file should be moved in a folder where there are present the following:
-- auth_logic folder
-- bussinessLogic

command to start the containers is: docker compose up --build

In order to deploy you need to move all deploy files in project folder and run command:
    kubectl apply -f app-service.yaml,db-service.yaml,kong-service.yaml,pgadmin-service.yaml,portainer-service.yaml,web-service.yaml,app-deployment.yaml,app-deployment.yaml,app-claim0-persistentvolumeclaim.yaml,db-deployment.yaml,postgres-data-persistentvolumeclaim.yaml,kong-deployment.yaml,kong-claim0-persistentvolumeclaim.yaml,pgadmin-deployment.yaml,portainer-deployment.yaml,data-persistentvolumeclaim.yaml,portainer-claim1-persistentvolumeclaim.yaml,web-deployment.yaml

Commands for k9s on bash:
   kubectl config get-contexts
   kubectl config get-contexts --kubeconfig=/mnt/c/Users/drago/.kube/config
   export KUBECONFIG=/mnt/c/Users/drago/.kube/config
   kubectl config get-contexts
   k9s