# rancher deploy rancher in kubernetes
```
helm repo add rancher-stable https://releases.rancher.com/server-charts/stable
```
```
Downlaod values.yaml
modify values.yaml 62,87
ingress.ingressClassName: "nginx"
```
```
helm install rancher rancher-latest/rancher --version 2.7.6 -f values.yaml \
  --namespace cattle-system \
  --set hostname=rancher.bivasdas.shop \
  --set ingress.tls.source=letsEncrypt \
  --set letsEncrypt.email=bivas0511@gmail.com
```
