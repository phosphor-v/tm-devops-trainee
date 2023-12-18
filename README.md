# Requirements
 - Amazon Web Services trial account.

## Amazon EFS:
Open AWS console and using search find *EC2*
In dashboard select security groups and click *Create security group*
![image](https://github.com/phosphor-v/tm-devops-trainee/assets/113942255/ceae75b4-259d-432a-a85e-38e9e6253f92)

On the page that opens give name of *SG*, add *description* and create *inbound/outbound rules* for *EFS* 

![image](https://github.com/phosphor-v/tm-devops-trainee/assets/113942255/83554c70-af78-4047-b9d1-c58ef9149f4b)


### Create an Amazon EFS file system named *tm-devops-trainee-efs*.
"
Open AWS console and using search find *EFS*
![image](https://github.com/phosphor-v/tm-devops-trainee/assets/113942255/ab948750-1150-4a35-9f26-60a68175a361)

On the page that opens, click *Create file system* and click on *Customize*
![image](https://github.com/phosphor-v/tm-devops-trainee/assets/113942255/88400e29-4379-4887-95e9-0a627a81fb81)


Give name of file system, change *Transition into Archive* setting to none and in *Performance settings* -> *Throughput mode* choose *Bursting* and click *next*.

![image](https://github.com/phosphor-v/tm-devops-trainee/assets/113942255/b8b0cf85-053a-410d-8ad7-5897345d2721)



### Ensure that the EFS file system is mounted on the ECS instances to store the HTML content.


### Use appropriate security settings for the EFS.


## Amazon ECS:
### Define an ECS task definition that runs a Docker container.


### Use a public Docker image of Nginx web server.


 ### Mount the EFS file system to the container to serve the HTML content.

 
### Configure the ECS service to run 1 task.


## ALB:
### Create an ALB named "tm-devops-trainee-alb."


### Configure the ALB listener on port 80 to forward traffic to the ECS service.


### Implement health checks on the ALB to ensure the ECS service's availability.


## Security Group:
### Create security groups for both the ECS instances and the ALB.


### Allow incoming traffic on port 80 to the ECS instances from the ALB.


### Configure appropriate security settings for the ALB.


## Web Application:
### Create a simple HTML page with the content: "Hello, Techmagic!"


### Upload this HTML page to the EFS file system.
