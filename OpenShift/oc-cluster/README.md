# Notes on Using oc cluster up

- Install [docker ce](https://docs.docker.com/install/)

- Edit */etc/docker/daemon.json*

```json
{
  "insecure-registries": "172.30.1.1:5000"
}
```

- Restart Docker

I believe that this is the *standard* address for the registry. The use of iptables ensures it is always correctly mapped.

The insecure registry is the internal OpenShift registry. Images will be pushed to this registry after they have been built.