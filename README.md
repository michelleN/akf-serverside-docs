# akf-serverside-docs

_Note: These docs are a work in progress_

## Overview
We have been given Azure credits to run our clusters on since we're a nonprofit.We have a small AKS cluster for development up and running where there is one instance of the backend node application running with sqlite. It is available via the IP address you can find in slack.

_TODO: Enable TLS_
_TODO: Deploy backend node application with a database running separately_

The backend node application is running in a Docker container on top of a Kubernetes cluster. _TODO: add links to relevant tech_

## Getting Started
You can hit the endpoint (find in slack) and the routes (find on backend node application repo) and get back some JSON to test against.

## Going Forward
The mobile app developers would like an endpoint to hit to get back some data and use for testing. This does not require a live, remote cluster. They can use [Draft](https://github.com/Azure/draft) to spin up an instance of the application running on a local Kubernetes cluster. They'll get a localhost url to test against and it will look and feel like just hitting a live, remote endpoint.

### Pre-requisites
Install Docker
Install and start Minikube
Install Helm and run `$ helm init` to set Helm up
Install Draft, run `$ draft init` and take a look at the getting started docs.
_TODO: insert links_
_TODO: add draft.toml file to backend node application repositoiry_

### Take Draft for a Spin
Use Draft to spin up build application Docker container and Deploy to local Kubernetes cluster (minikube)

In your terminal and in the source code directory:
```console
$ draft up # containerize and deploy application
$ draft connect # gets you a localhost url to point to and test against
```
