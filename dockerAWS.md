### Deploying dockerized application to AWS

https://www.youtube.com/watch?v=3Pk4Cma04pU&ab_channel=ScalableScripts

1. Build image
        
        $ docker build -t APP_NAME .
        
2. Log into AWS

        $ aws ecr get-login-password --region region | docker login --username AWS --password-stdin ACCOUNT_ID.dkr.ecr.region.amazonaws.com
        
3. Tag and push

        $ docker tag APP_NAME ACCOUNT_ID.dkr.ecr.region.amazonaws.com/APP_NAME:latest
        $ docker push ACCOUNT_ID.dkr.ecr.region.amazonaws.com/APP_NAME:latest
        
### After Deploy

The following steps don't actually change anything. Just create a new service with the same name. Take note, the `IP Address` changes everytime you create a new service.

- Go to cluster and service.
- Select service and click update.
- Set number of tasks as 0 and update.
- After deployment is finished, re-scale number of tasks to 1.
 
