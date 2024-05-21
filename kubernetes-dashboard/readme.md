# comandos para instalar o kubernetes-dashboard

```bash
helm repo add bitnami https://charts.bitnami.com/bitnami

helm upgrade --install kubernetes-dashboard kubernetes-dashboard/kubernetes-dashboard --create-namespace --namespace kubernetes-dashboard

kubectl apply -f service-account.yaml

kubectl -n kubernetes-dashboard create token admin-user

kubectl -n kubernetes-dashboard port-forward svc/kubernetes-dashboard-kong-proxy 8443:443
```