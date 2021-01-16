# Kubernetes - Setel Asessment

this project shows example of deploying Setel app using Kubernetes. We will have 3 services (including 1 SPA react-app) and also postgresql service as the database. All of the service is already being hosted at DockerHub

- [Order Service](https://hub.docker.com/repository/docker/faridul/so-app)
- [Payment Service](https://hub.docker.com/repository/docker/faridul/sp-app)
- [SPA application](https://hub.docker.com/repository/docker/faridul/sa-spa)

**Requirement**

- Docker
- Minikube
- Kubectl

**Quick Start**

  build for both `db` and `app` folder by running:
  ```shell
  $ kubectl apply -f db/
  $ kubectl apply -f app/
  ```
  this will build all the necessary delpoyment and service.

  next run migrations on both `order` and `payment` service:

  ```shell
  $ kubectl exec <namespace> npm run reset 
  ```

  you can get the pod name by running:

  ```shell
  $ kubectl get pods
  ```

  TBC....