# Notes on Using oc cluster up

- Install [docker ce](https://docs.docker.com/install/)

- Edit */etc/docker/daemon.json*

```json
{
  "insecure-registries": "172.30.1.1:5000"
}
```

Not sure how to figure out the IP address to use yet.

The insecure registry is the internal OpenShift registry. Images will be pushed to this registry after they have been built.