This repository includes cloud cost optimization strategies that one can implement to reduce their AWS cloud cost effectively. 

Strategies included are:

1. Stale EBS snapshot deletion - Any stale snapshot of EBS volume increase the storage cloud cost, thus, one can optimize their cost by deleting these stale snapshots. Here, we use Lambda function for running the program, boto3 as a libraryto communicate with AWS API. Lambda function here is expected to be triggered manually, but one can also use cloudwatch to create a cronJob (EventBridge Scheduler) to run this program as per schedule required. 

  
