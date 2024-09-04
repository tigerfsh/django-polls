# Django Tutorial Polls App (Dockerized)

This repository contains the complete code for the [Django](https://www.djangoproject.com/) project's [tutorial](https://docs.djangoproject.com/en/2.1/intro/tutorial01/) `polls` app. The code should mirror the code you've written at the end of [Part 7](https://docs.djangoproject.com/en/2.1/intro/tutorial07/). 

In this branch of the repository, the Django project code has been modified to work in a Docker-based environment, as described in [How to Build a Django and Gunicorn Application with Docker](https://www.digitalocean.com/community/tutorials/how-to-build-a-django-and-gunicorn-application-with-docker).

Sensitive variables in the `env` file have been scrubbed. Instructions for filling in these configuration variables are available in the accompanying DigitalOcean [tutorial](https://www.digitalocean.com/community/tutorials/how-to-build-a-django-and-gunicorn-application-with-docker)

This app is meant to be used as a reference Django app for several DigitalOcean tutorials, and should not be deployed in production.

----

### Quickstart

To learn how to build and run the `polls` app container image, consult [How to Build a Django and Gunicorn Application with Docker](https://www.digitalocean.com/community/tutorials/how-to-build-a-django-and-gunicorn-application-with-docker).


### Test
 curl --resolve "hello.polls.com:80:$( minikube ip )" -i http://hello.polls.com

### kubectl version

Client Version: v1.31.0
Kustomize Version: v5.4.2
Server Version: v1.30.0


### tk & jb 

#### install tk & jb
sudo curl -Lo /usr/local/bin/tk https://github.com/grafana/tanka/releases/latest/download/tk-linux-amd64
sudo chmod a+x /usr/local/bin/tk

sudo curl -Lo /usr/local/bin/jb https://github.com/jsonnet-bundler/jsonnet-bundler/releases/latest/download/jb-linux-amd64
sudo chmod a+x /usr/local/bin/jb

#### install k8s-libsonnet
tk init
jb install github.com/jsonnet-libs/k8s-libsonnet/1.21@main github.com/grafana/jsonnet-libs/ksonnet-util


### Doc about Tanka
https://tanka.dev/jsonnet/overview/


### Create secret
kubectl create secret generic polls-secret --from-env-file=polls-secrets

