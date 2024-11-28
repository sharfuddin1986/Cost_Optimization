# AWS Cloud Cost Optimization - Identifying Stale Resources

**Identifying Stale EBS Snapshots**

In this example, we'll create a Lambda function that identifies EBS snapshots that are no longer associated with any active EC2 
instance and deletes them to save on storage costs.


**Description:**
The Lambda function fetches all EBS snapshots owned by the same account ('self') and also retrieves a list of active EC2 instances 
(running and stopped). For each snapshot, it checks if the associated volume (if exists) is not associated with any active instance. 
If it finds a stale snapshot, it deletes it, effectively optimizing storage costs.

**condition**
1-Ebs volume is connected with ec2 instance.Taking a snapshot of ebs volume.

2- if ec2 instanc is deleted and volume is also deleted snapshot is not deleted bymistake.Then its unnessacary charges need to 
   optimize trigger the lambda function.its check condition any snaphot is not match with volume ya instance its deleted


![3](https://github.com/user-attachments/assets/331d621b-d59b-4766-a05a-7d774feaead7)
