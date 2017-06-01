# Croc Hunter - The game!

For those that have dreamt to hunt crocs

# Usage
Basic go webserver to demonstrate example CI/CD pipeline using Kubernetes

# Deploy using Jenkins Chart and Helm
[![Demo Pipeline](https://img.youtube.com/vi/NVoln4HdZOY/0.jpg)](https://youtu.be/NVoln4HdZOY "Demo Pipeline")

# How to setup the Jenkins infrastructure
[![Jenkins Setup](https://img.youtube.com/vi/eMOzF_xAm7w/0.jpg)](https://youtu.be/eMOzF_xAm7w "Jenkins Setup")
* See DEMO.md for steps

# How to deploy using Draft
[Draft](https://github.com/Azure/draft) is a tool for developers to create cloud-native applications on Kubernetes.

If you have an existing Kubernetes cluster on a cloud provider, Draft is the fastest way to containerize, package, and deploy croc-hunter to Kubernetes.

## Prerequisites
- Draft will need a cloud-provided Kubernetes cluster to deploy your app. It's possible to use Minikube, but Draft requires a wildcard domain and an ingress controller which can be difficult to set up properly on one's laptop.
- [Install Helm](https://github.com/kubernetes/helm/blob/master/docs/install.md) onto your cluster
- Install an ingress controller on your Kubernetes cluster using Helm: `helm install stable/nginx-ingress`
- Draft needs to push images to a Docker registry, so you'll need to configure Draft with your Docker registry credentials. If you don't already have one, you can create a Docker registry for free on either Docker Hub or Quay.io.

1. Clone the repo
1. `draft create` to containerize croc-hunter based on the Draft go packs
1. `draft up` to deploy your application to a Kubernetes dev sandbox, accessible via a public URL
1. Use a local editor to modify the application, with changes deployed to Kubernetes in seconds
