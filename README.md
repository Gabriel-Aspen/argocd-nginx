# argo-nginx

### download Argo CD
kubectl create namespace argocd
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
### Access Argo CD UI
kubectl port-forward svc/argocd-server -n argocd 8080:443
hop onto localhost:8080

### Deploying apps
kubectl apply -f argo-nginx-staging.yaml
kubectl apply -f argo-nginx-prod.yaml

### Make sure to sync the apps
