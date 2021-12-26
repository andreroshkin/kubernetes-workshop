docker build -t andreroshkin/demo:0.0.1 .
docker images
docker tag demo andreroshkin/kube:0.0.1
docker push andreroshkin/demo:0.0.1


kubectl config get-contexts
kubectl config use-context docker-desktop
kubectl create secret docker-registry myregistry --docker-server=docker.io --docker-username= --docker-password= --docker-email=

kubectl apply -f deploy.yaml

kubectl get pods

kubectl get deployment

kubectl expose deployment demo --type=NodePort

kubectl get service

kubectl scale --current-replicas=2 --replicas=3 deployment/demo

kubectl delete -f deploy.yaml

kubectl delete service demo
