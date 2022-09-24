Rancher Desktop use different networking on macOS and Linux. On macOS it yuse bridge mode and on Linux it use nat mode. For a linux installation you need to use the abow Provisioning Script.


Before you start your Rancher Desktop the first time do this:
```bash
mkdir -p ~/.local/share/rancher-desktop/lima/_config/
cp 0_linux/override.yaml ~/.local/share/rancher-desktop/lima/_config/override.yaml
```

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
