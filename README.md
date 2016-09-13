# kubernetes-images-amd64

Kubernetes images ready for "docker load" on a host not connected to the Internet.

Example creation:
```
$ docker pull gcr.io/google_containers/kubernetes-dashboard-amd64:v1.4.0-beta1
$ docker save gcr.io/google_containers/kubernetes-dashboard-amd64:v1.4.0-beta1 | gzip - > kubernetes-dashboard-amd64-v1.4.0-beta1.tar.gz
```

Example load:

```
$ gzip -dc kubernetes-dashboard-amd64-v1.4.0-beta1.tar.gz | docker load
```

