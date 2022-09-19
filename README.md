

### Local docker registry
```bash
nerdctl login
nerdctl pull nginx
nerdctl tag nginx registry.rancher-decktop.intra/nginx:1.0
nerdctl push registry.rancher-decktop.intra/nginx:1.0
nerdctl --namespace k8s.io image pull registry.rancher-decktop.intra/nginx:1.0
```


```bash
oras pull ghcr.io/aquasecurity/trivy-db:2

oras push -d docker.rancher-decktop.intra/trivy-db:2 \
./db.tar.gz:application/vnd.aquasec.trivy.db.layer.v1.tar+gzip
```
