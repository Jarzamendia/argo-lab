# Instalar Argo
kubectl create namespace argocd
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml

# Instalar Istio
istioctl install --set profile=default -y
kubectl apply -f samples/addons

## Acessar dashboard
istioctl dashboard kiali

# TODO
kubectl label namespace bookinfo istio-injection=enabled