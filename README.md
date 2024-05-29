aws eks --region us-east-1 update-kubeconfig --name exam3-cluster

kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
kubectl get deployments
kubectl get pods
kubectl describe deployments
kubectl rollout status deployment/my-app
kubectl describe deployment my-app

kubectl patch deployment/my-app -p "{\"spec\":{\"progressDeadlineSeconds\":6000}}"
kubectl run my-app --image=my-app --namespace=kube-system 

kubectl config set-context --current --namespace=kube-system
