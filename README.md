Kubernetes-test
-deploying apps
    kubectl -f name -n namespace
-services
    load balancer: outside 
    clusterIP: internal networking
    NodePort: send to only one or a specific expressed in the service

    

Getting ArgoCD
create namespace for ArgoCD
	-kubectl create namespace argocd
apply argocd deployment
	-kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
Port forward to access the server
	-kubectl port-forward -n argocd svc/argocd-server 8080:443
Getting initial password
	-kubectl get secrets argocd-initial-admin-secret -n argocd -o yaml
Decode first password in Bash
	-echo aGdCMExpVnBER0o1UVRQQw== | base64 -d
    
PORT FORWARD
-kubectl port-forward -n argocd svc/argocd-server 8080:443

HELM CHARTS
