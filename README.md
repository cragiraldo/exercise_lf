# exercise_lf

This resolucion from exercise form document [LFDevOpsExecise.pdf](media/LFDevOpsExercise.pdf)

## Problem 1  
### answer question 1
- architecture  

![test](media/exercise_lf_arq-monolithic.drawio.png)  

### answer question 2
- The architecture has 2 availability zones where requests will be centralized through a Load Balancer application, which will validate the node's health and forward all requests in the event of a crash of one of the instances.  

### answer question 3  
- The databases are linked through rds proxy which will have a target group of databases where it will promote the passive database from reading to writing automatically in case of inconsistencies in the writing database.  

### answer question 4  
- 