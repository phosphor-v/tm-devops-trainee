[Final result](http://tm-devops-trainee-alb-1714219327.eu-north-1.elb.amazonaws.com/), **text me if down**
# Deploy instructions:
### Open AWS console and navigate to *CloudFormation*, then click on *Create Stack*
![image](https://github.com/phosphor-v/tm-devops-trainee/assets/113942255/899ae8d9-fbcb-455a-a024-32223abb6e7f)
### Select *Upload template file* then upload task.yaml and click *Next*
![image](https://github.com/phosphor-v/tm-devops-trainee/assets/113942255/3c4397ed-01f8-4fa4-9e07-f919ecad8056)
### Give name of stack and click *next* to last page a place mark in information sentence before click on *Sumbit*
![image](https://github.com/phosphor-v/tm-devops-trainee/assets/113942255/b53d01ce-3352-4529-b56e-2ed75488cd68)
![image](https://github.com/phosphor-v/tm-devops-trainee/assets/113942255/f93dca92-c168-48a3-be35-53a86b23a9e9)
### Wait for the resources to be created
![image](https://github.com/phosphor-v/tm-devops-trainee/assets/113942255/e69761ee-1c84-499f-acce-867361c3ee29)
### After creation you will see **CREATE_COMPLETE**
![image](https://github.com/phosphor-v/tm-devops-trainee/assets/113942255/03bea937-305f-4e18-9025-a8ca09b967d5)
### Navigate to *Outputs* and click on *LoadBalancerURL valoue*
![image](https://github.com/phosphor-v/tm-devops-trainee/assets/113942255/8f332429-e51c-447b-9915-a6dc0530846a)
### You will see this page
![image](https://github.com/phosphor-v/tm-devops-trainee/assets/113942255/b6ad3009-c1c6-41c4-a42b-9e1745f9d2c4)

# The difficulties I encountered:
 **Issue**: Failed to resolve server us-east-1a.fs-c2aXXXX.efs.us-east-1.amazon
aws.com: Name or service not known


 **Solution**: [enable dns hostnames](https://github.com/phosphor-v/tm-devops-trainee/blob/ad28a867ec901eef06f5257d7056b158a1c1d20b/task.yaml#L8)https://github.com/phosphor-v/tm-devops-trainee/blob/ad28a867ec901eef06f5257d7056b158a1c1d20b/task.yaml#L8

 
 **Issue**: index.html creation in EFS

 
 **Solution**: Used [AWS Lambda function](https://github.com/phosphor-v/tm-devops-trainee/blob/389aa2e3b6c142255d5e848ebca5bbe57830a7a1/task.yaml#L217)https://github.com/phosphor-v/tm-devops-trainee/blob/389aa2e3b6c142255d5e848ebca5bbe57830a7a1/task.yaml#L217-L257 with [Custom Resource to invoke](https://github.com/phosphor-v/tm-devops-trainee/blob/389aa2e3b6c142255d5e848ebca5bbe57830a7a1/task.yaml#L258)https://github.com/phosphor-v/tm-devops-trainee/blob/389aa2e3b6c142255d5e848ebca5bbe57830a7a1/task.yaml#L258-L264
