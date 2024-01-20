# Argo CD Setup

## Installed Argo CD

```
kubectl create namespace argocd
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
```

## Ran Argo CD in HTTP Mode(Insecure)

https://github.com/argoproj/argo-cd/blob/54f1572d46d8d611018f4854cf2f24a24a3ac088/docs/operator-manual/argocd-cmd-params-cm.yaml#L82

## Exposed Argo CD Server Service in NodePort Mode

```
kubectl edit svc argocd-server -n argocd
```

and changed the type to NodePort from ClusterIP

