# Homepage Kubernetes

Simple static homepage deployed on Kubernetes.

## Features

- nginx container
- 2 replicas
- NodePort service
- HTML delivered via ConfigMap
- GitOps deployment via ArgoCD


# ikony na nfsie
```
kubectl cp ../../../icons/helpdesk.svg  polcom/homepage-5466f6d7b9-k99tx:/usr/share/nginx/html/icons
kubectl rollout restart deployment homepage -n polcom
 kubectl exec -it homepage-86c6d65c46-d2hq5 -n polcom -- ls /usr/share/nginx/html/icons
 kubectl cp ../../../icons/grafana.svg  polcom/homepage-86c6d65c46-d2hq5:/usr/share/nginx/html/icons/
 kubectl cp ../../../icons/proxmox.svg  polcom/homepage-86c6d65c46-d2hq5:/usr/share/nginx/html/icons/
 kubectl cp ../../../icons/helpdesk.svg  polcom/homepage-86c6d65c46-d2hq5:/usr/share/nginx/html/icons/
 kubectl rollout restart deployment homepage -n polcom

```
