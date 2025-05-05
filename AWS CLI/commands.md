Install AWS CLI in local system and it requires Acess key and secret key from IAM user to authenticate.
if you are performing AWS CLI in AWS tool, then use AWS Cloudshell option which doean't needs acess key and secret key for authentication.

Aws --version
aws configure to authenticate with generated keys
aws s3 ls
aws ec2 describe-instances --region us-east-2

instance_id="i-05a15f6750a088254"
aws ec2 describe-instance-status --instance-id $instance_id \
  --query 'InstanceStatuses[*].InstanceState.Name' --output text

instance_id="your-db-instance-id" 
aws rds describe-db-instances --db-instance-identifier $instance_id --query 'DBInstances[*].DBInstanceStatus' --output text

aws ec2 start-instances --instance-id i-05a15f6750a088254
aws ec2 stop-instances --instance-id i-05a15f6750a088254


How would you write a script to stop all EC2 instances in a region?

#!/bin/bash
instances=$(aws ec2 describe-instances --query \
  "Reservations[*].Instances[*].InstanceId" --output text)

for id in $instances; do
  aws ec2 stop-instances --instance-ids "$id"
done
