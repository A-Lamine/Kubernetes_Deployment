# Kubernetes Deployment

<h1 align="center">
    <img src="https://sp-ao.shortpixel.ai/client/to_auto,q_lossy,ret_img,w_950,h_842/https://www.blackcreeper.com/wp-content/uploads/2020/04/kubernetes-logo-big.png" width=300 height=250>
</h1>

## Start up the Redis Database


### Creating the Redis Deployment :
    
<h1 align="center">
    <img src="./pics/db-deploy.png">
</h1>
    
    Apply the Redis Deployment from the redis-leader-deployment.yaml file:
    kubectl apply -f .\redis-deploy.yaml

    verification of our deployments
    kubectl get deploy
<img src="./pics/check-db-deploy.png">

### Creating the Redis service :
    
<h1 align="center">
    <img src="./pics/db-service.png">
</h1>
    
    Apply the Redis Service from the following redis-leader-service.yaml file:
    kubectl apply -f .\redis-service.yaml

    verification of our service
    kubectl get svc
<img src="./pics/check-db-service.png">

### Set up Redis followers :

<h1 align="center">
    <img src="./pics/backend-deploy.png">
</h1>

    Apply the Redis Deployment from the following redis-follower-deployment.yaml file:
    kubectl apply -f .\redis-follower-deployment.yaml

    verification of our deploy
    kubectl get deploy

<img src="./pics/check-backend-deploy.png">

### Creating the Redis follower service :

<h1 align="center">
    <img src="./pics/backend-service.png">
</h1>

    Apply the Redis Service from the following redis-follower-service.yaml file:
    kubectl apply -f .\redis-follower-service.yaml

    verification of our service
    kubectl get deploy

<img src="./pics/check-backend-service.png">

## Set up and Expose the Guestbook Frontend

### Creating the Guestbook Frontend Deployment :

<h1 align="center">
    <img src="./pics/frontend-deploy.png">
</h1>

    Apply the frontend Deployment from the frontend-deployment.yaml file:
    kubectl apply -f .\frontend-deployment.yaml

    verification of our deployment
    kubectl get deploy

<img src="./pics/check-frontend-deploy.png">

### Creating the Frontend Service :

<h1 align="center">
    <img src="./pics/frontend-service.png">
</h1>

    Apply the frontend Deployment from the frontend-deployment.yaml file:
    kubectl apply -f .\frontend-service.yaml

    verification of our service
    kubectl get service

<img src="./pics/check-frontend-service.png">

Go to http://localhost:80 AND Enjoy :call_me_hand:

<img src="./pics/Result.png">

    


