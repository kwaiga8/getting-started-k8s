# Readme

Node.js web app for use in Pluralsight [Getting Started with Kubernetes](https://app.pluralsight.com/library/courses/getting-started-kubernetes/table-of-contents) video course.

Packages and dependencies will be upadted annually. May contain vulnerable code, **use at own risk**.

## App

The app, dependencies, and Dockerfile are in the `/App` folder.

## Kubernetes YAML files

All Kubernetes YAML manifests are in the `Pods`, `Services`, and `Deployments` folders.

## Additional references

List of additional books, courses, blogs, and other places this repo is used/referenced:

- None

## Pre-created image

A publically available pre-created container image is available for download [here](https://hub.docker.com/repository/docker/nigelpoulton/getting-started-k8s)

## INSTRUCTIONS to run (single pod):
- docker image build -t nigelpoulton/getting-started-k8s:1.0 .
- docker image push nigelpoulton/getting-started-k8s:1.0
- cd Pods
- kubectl apply -f pod.yml
- kubectl get pods --watch or kubectl get pods -o wide

delete cluster:
- kubectl delete -f pod.yml
 