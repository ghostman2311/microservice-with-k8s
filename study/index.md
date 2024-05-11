# 11 May

## Introducing deployments

1. Deployment manages the pods
   ![alt text](image.png)

## Creating deployments

1. create posts-depl.yaml in infra/k8s
   ![alt text](image-1.png)

2. Common Command around deployments
   ![alt text](image-2.png)

## Updating deployments

1. This is not the recommended way

- Make changes to source code.
- Build the docker image with updated version.
- Update the deployment yaml.
- Run kubectl apply -f command
- That's it.

2. Problem is we should not update the deployment file very often. Each time we make changes to the source code we have to change the version in deployment file.

## Preferred method for updating deployments

1. Here is the recommended way
   ![alt text](image-3.png)

2. Remove imageNever pull policy.

## Networking with services

1. 4 different types of services we need to be aware of
   ![alt text](image-4.png)

## Creating a NodePort service

1. Create posts-srv.yaml in k8s
   ![alt text](image-5.png)
