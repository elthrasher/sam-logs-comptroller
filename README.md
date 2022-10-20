# SAM Logs Comptroller

## :warning: This construct is designed to delete logs and log groups! **Use at your own risk!**

This is the [AWS SAM](https://aws.amazon.com/serverless/sam/) version of [AWS Logs Comptroller](https://github.com/elthrasher/aws-logs-comptroller). This is a Lambda-less Step Functions-only application that can run at intervals to set CloudWatch LogGroup Retention as well as prune "orphaned" Lambda logs and keep your CloudWatch tidy.

## App Parameters
1. EnableScheduler (default `False`) - whether or not to schedule the state machine.
2. RetentionInDays (default `7`) - Log retention to set for LogGroups that do not have retention set.
3. Schedule (default `rate(7 days)`) - A [Schedule Expression](https://docs.aws.amazon.com/eventbridge/latest/userguide/eb-create-rule-schedule.html) for running the scheduler (only important if scheduling is enabled).

