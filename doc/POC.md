### Розгортання Argo CD на кластері k3d

Create cluster<br>
`k3d cluster create argo`

Create namespace<br>
`kubectl create namespace argocd`
 
Apply Argo CD<br>
`kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml`

Port-forward<br>
`kubectl port-forward svc/argocd-server -n argocd 8080:443&`

Url home page<br>
[https://127.0.0.1:8080](https://127.0.0.1:8080)

Get admin password in decoding Base64<br>
`kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d; echo`

## Demo

![Demo](/.data/argo_install.gif)