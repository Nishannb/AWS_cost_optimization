Under AWS Cloud Cost Optimization: Identifying Stale EBS snapshots Resources (Unused)

Here, we are using boto3 library to communicate with AWS API for fetching information on running EC2 instances, volume associated with it and also snapshots of those volumes. 

Here, we try to optimize the AWS cost by deleting the EBS snapshots that are no longer associated with any running/active EC2 instances.

Process:
1. Lambda function fetches all the EBS snapshots and EC2 instances(active) owned by the account (denoted   by 'self' as in code implementation).
2. Looping for each snapshot, program checks whether any volume associated with it exist or not and also checks whether it(respective volume) is associated with any active instance, if no, it considers those EBS snapshots as stale and delete it.
