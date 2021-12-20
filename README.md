# exercise_lf

This resolucion from exercise form document [LFDevOpsExecise.pdf](media/LFDevOpsExercise.pdf)

## Problem 1  
### answer question 1
- architecture  

![test](media/exercise_lf_arq-monolithic.drawio.png)  

### answer question 2
- The architecture has 2 availability zones where requests will be centralized through a Load Balancer application, which will validate the node's health and forward all requests in the event of a crash of one of the instances.  

### answer question 3  
- The database cluster are linked through rds proxy which will have a database target, where it will promote the passive database from read to write automatically in case of inconsistencies in the write database in one of the zones availability.  

### answer question 4  
- For the implementation of a Disaster Recovery it is suggested to implement a 'Warm standby' architecture where the traffic between regions is supported from 'Route 53'. The architecture would be deployed and it would remain active with data replication at the 'RDS Aurora' level and for the uniform deployment, a golden AMI is used with the provisioning of dependencies from the deployment. For a disaster recovery from 'Route 53', the region's traffic is redirected through a health check configuration. where the infrastructure already has active ec2 machines and a replicated database. estimated recovery time 10 min.  