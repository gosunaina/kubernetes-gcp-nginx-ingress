# kubernetes-gcp-nginx-ingress

A standard nginx/gcp-lb ingress template with Datadog monitoring

Put your actual k8s/ingress mappings in the templates/ingress/ingress.yaml !

Customise settings or create a new default env

Relies on `go get github.com/AlexsJones/vortex` for interpolation of env

```
./build_environment.sh default
kubectl create -f deployment/
```


Includes `configmap-defaultconf.yaml` to show how you can extend upon the default nginx config

## Datadog

This example loads the DD agent as a sidecar container. You can just remove this and it will all work without it.

Requires `environments/default.yaml` datadog key to be set!
