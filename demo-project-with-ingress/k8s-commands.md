### minikube apply commands in order to pull required images
    minikube image pull mongo
    minikube image pull mongo-express
    minikube addons enable ingress

### kubectl apply commands in order

    kubectl apply -f namespace-dev.yaml
    kubectl apply -f mongo-secret.yaml
    kubectl apply -f mongo.yaml
    kubectl apply -f mongo-configmap.yaml
    kubectl apply -f mongo-express.yaml
    kubectl apply -f development-ingress.yaml

### kubectl get commands

    kubectl get pod
    kubectl get pod --watch
    kubectl get pod -o wide
    kubectl get service
    kubectl get secret
    kubectl get all | grep mongodb

### kubectl debugging commands

    kubectl describe pod mongodb-deployment-xxxxxx
    kubectl describe service mongodb-service
    kubectl logs mongo-express-xxxxxx

### give a URL to external service in minikube

    minikube service mongo-express-service -n development
    minikube ip
    copy the output (will be the external IP)
    go to /etc/hosts
    paste the fallowing to the end 
    externalIP  demodb.com
    go to demodb.com from your browser

