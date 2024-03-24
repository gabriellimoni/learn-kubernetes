# API endpoints

The examples below are after applying the `wordpress` setup in this repo.

First of all we need to define which namespace we are working on. For the examples we'll use the `default`.

Secondly, if using `minikube` run `kubectl proxy --port=8080` to setup your cluster proxy.

1. List nodes: `http://127.0.0.1:8080/api/v1/nodes`
1. List services: `http://127.0.0.1:8080/api/v1/namespaces/default/services/`
1. Get service: `http://127.0.0.1:8080/api/v1/namespaces/default/services/wordpress`
1. List pods from service via `labelSelector`: `http://127.0.0.1:8080/api/v1/namespaces/default/pods?labelSelector=tier=frontend,app=wordpress`
1. List deployments: `http://127.0.0.1:8080/apis/apps/v1/namespaces/default/deployments`
1. Get deployment: `http://127.0.0.1:8080/apis/apps/v1/namespaces/default/deployments/wordpress`
1. List replica sets via `labelSelector`: `http://127.0.0.1:8080/apis/apps/v1/namespaces/default/replicasets?labelSelector=app=wordpress,tier=frontend`
