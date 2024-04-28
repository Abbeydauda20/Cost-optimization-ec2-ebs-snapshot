# AWS Cloud Cost Optimization - Identifying Stale Resources

## Identifying Stale EBS Snapshots

In this example, we'll create a Lambda function that identifies EBS snapshots that are no longer associated with any active EC2 instance and deletes them to save on storage costs.

### Description:

The Lambda function fetches all EBS snapshots owned by the same account ('self') and also retrieves a list of active EC2 instances (running and stopped). For each snapshot, it checks if the associated volume (if exists) is not associated with any active instance. If it finds a stale snapshot, it deletes it, effectively optimizing storage costs.

Take snapshot every hour and retain for 24 hours
Take snapshot at the end of day take a snapshot for the entire day and keep for one week
Take snapshot at the end of week and retain for one month
Take snapshot at the end of month and keep for 12 month
Take snapshot at the end of year and retain for 7 years


