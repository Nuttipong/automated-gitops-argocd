Requirements for Argo CD
1. kubectl command-line tool
2. Kubernetes cluster to host Argo CD
3. Cluster admin level access
4. kubeconfig configured to connect Kubenetes cluster
5. Access to Github or other repo

Deploying Argo CD

Types of Argo CD install
Non HA, 
- install.yaml
- recommended for dev
- single pods, replicas for Argo CD
HA,
- namespace-install.yaml
- recommended for prod
- Tuned for HA and resiliency
- multiple replicas for suppoted components
Core install,
- core-install.yaml
- lightweigh
- no webui, API server not needed

Cluster level
- Use when you have cluster level access & will deploy apps in the same cluster
that Argo CD runs on.
Namespace level
- Use when you have namespace level access & will deploy apps external cluster
from where Argo CD running

```
> k create namespace argocd
> k apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
> k port-forward service/argocd-server 8080:80
```

Reset pwd
- https://argo-cd.readthedocs.io/en/release-1.8/faq/



Accessing Argo CD API Server
1. WebUI
2. Argo CD CLI
```
> choco install argocd-cli
> brew install argocd
```
Common CLI
```
> argocd login
> argocd account
> argocd proj
> argocd app
> argocd repo
> argocd version
> argocd-util
> argocd cluster
```


Using CLI
```
```

Upgrading Argo CD
```
```

Setting up RBAC for Argo CD
```
```

Configuring user mgmt in Argo CD
Setting up secret mgmt with Argo CD
HA, Backup, and Disaster recovery 
Webhook
Monitoring and Notification