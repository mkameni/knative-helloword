### Knative demo

```bash
    $ kubectl create clusterrolebinding cluster-admin-binding --clusterrole=cluster-admin --user=$(gcloud config get-value core/account)
```

```bash
    $ kubectl apply -f https://storage.googleapis.com/build-crd/latest/release.yaml
```

```bash
    $ kubectl -n knative-build get pods -w
```

```bash
    $ kubectl get crd
```

```bash
    $ kubectl apply -f secret.yaml
```

```bash
    $ kubectl apply -f service-account.yaml
```

```bash
    $ kubectl apply -f build.yaml
```

```bash
    $ kubectl logs docker-build-XXXXX -c build-step-build-and-push
```

```bash
    $ kubectl describe builds
```