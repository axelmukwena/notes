1. Build image
        
        $ docker build -t APP_NAME .
        
2. Log into AWS

        $ aws ecr get-login-password --region region | docker login --username AWS --password-stdin ACCOUNT_ID.dkr.ecr.region.amazonaws.com
        
3. Tag and push

        $ docker tag APP_NAME ACCOUNT_ID.dkr.ecr.region.amazonaws.com/APP_NAME
        $ docker push ACCOUNT_ID.dkr.ecr.region.amazonaws.com/APP_NAME
 
