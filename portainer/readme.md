# comandos para instalar o kubernetes-dashboard

```bash
helm repo add portainer https://portainer.github.io/k8s/

helm upgrade --install --create-namespace -n portainer portainer portainer/portainer --set tls.force=true

kubectl -n portainer port-forward svc/portainer 9000:9000
```