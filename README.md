# Spring Kubernestes project
### in this task we build a docker image for spring-website that include a database (mysql server)
- step 1 (DockerFile): 
    - we create a DockerFile 
    - we build the image using this command "docker build . -t shadifadila/my_repo:spring"
    - we upload the image to dokcerhub : 
        - the image avaible on this path : 
            shadifadila/my_repo:spring
- step 2 (Kubernetes) : 
    there is theee files 
        - spring-configmap.yaml 
            ###### for mysql environment variables
        - spring-deployment.yaml
            include two conatiners in the same POD, the first container is for mysql and the second for spring-website
        - spring-service.yaml 
            network - the service allow us to connect to the pod(spring - website)
        
    run-command : 
        kubectl apply -f ./Kubernetes/
    
    delete commnad : 
        kubectl delete svc,pods,deployments,configmap --all 
- step 3 : jenkines 

    screenshot : 



    
