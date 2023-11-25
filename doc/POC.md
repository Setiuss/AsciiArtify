### Argo CD 

Create cluster
`k3d cluster create argo`

Create namespace
`kubectl create namespace argocd`
 
Apply Argo CD
`kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml`

Port-forward
`kubectl port-forward svc/argocd-server -n argocd 8080:443&`

Url home page
[https://127.0.0.1:8080](https://127.0.0.1:8080)

Get admin password in decoding Base64
`kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d; echo`

## Demo

![Demo](/.data/argo_install.gif)