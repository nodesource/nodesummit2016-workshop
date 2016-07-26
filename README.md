## NodeSummit N|Solid, Docker & Kubernetes Workshop

This repo is to help setup the dependencies for the workshop. It assumes you received an USB drive. This is in an attempt to not over saturate the wifi network during the conference.

If you are not at the conference please refer to: [nodesource/nsolid-kubernetes](https://github.com/nodesource/nsolid-kubernetes)

### Mount USB disk

Verify you can see the volume on your computer.

### Install Docker

If you don't have `Docker` installed, use the installer located inside your OS folder on the flash drive.

**NOTE:** If your running linux download from [Linux Install](https://docs.docker.com/engine/installation/linux/)

### Install VirtualBox

If `VirtualBox` is not installed, use the installer located inside your OS folder on the flash drive.

**NOTE:** If your running linux download from [Linux Downloads](https://www.virtualbox.org/wiki/Linux_Downloads)


### Import Docker images

From the command line change directories to the root of the usb mount.

Make sure docker is running before running.

```bash
docker import images/gcr.io/google_containers/kube-cross_v1.6.2-1.tar.gz gcr.io/google_containers/kube-cross:v1.6.2-1
docker import images/gcr.io/google_containers/kube-addon-manger-amd64_v2.tar.gz gcr.io/google_containers/kube-addon-manager-amd64:v2
docker import images/gcr.io/google_containers/kubernetes-dashboard-amd64_v1.1.0.tar.gz gcr.io/google_containers/kubernetes-dashboard-amd64:v1.1.0
docker import images/gcr.io/google_containers/pause-amd_3.0.tar.gz gcr.io/google_containers/pause-amd64:3.0

docker import images/nodesource/nsolid_v1.4.0.tar.gz nodesource/nsolid:v1.4.0
docker import images/nodesource/nsolid-console_v1.7.3.tar.gz nodesource/nsolid-console:v1.7.3
docker import images/nodesource/nsolid-hub_v4.0.0.tar.gz nodesource/nsolid-hub:v4.0.0
docker import images/nodesource/nsolid-registry_latest.tar.gz nodesource/nsolid-registry:latest

docker import images/nginx_latest.tar.gz nginx:latest
```

### Install kubectl

Change directory to your OS directory within the USB mounted drive.

```bash
sudo cp kubectl /usr/local/bin && chmod +x /usr/local/bin/kubectl
```

### Install minikube

Change directory to your OS directory within the USB mounted drive.

```bash
sudo cp minikube /usr/local/bin && chmod +x /usr/local/bin/minikube
```
