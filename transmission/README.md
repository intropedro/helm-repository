# Transmissión

Transmission Chart to Kubernettes

# Instalación

The first is add ther repositorio to helm:

```shell
helm repo add intro https://helm.intropedro.com
helm repo update
```
And now we install it:

``` shell
helm install intro/transmission
```


Example using secret, pvc and node selector by node name:

``` shell
helm install transmission \
  --set secrets.use=true \
  --set secrets.name=SECRETP_NAME \
  --set secrets.key=PASSWORD_NAME \
  --set volumes.downloads=CUSTOM_PATH \
  --set volumes.watch=CUSTOM_PATH \
  --set volumes.config.userHostPath=false \
  --set volumes.config.userPVC=true \
  --set volumes.config.claimName=PVC_NAME \
  --set nodeName=NODE_NAME
```


