# Monitoring the Progress of a Stack Update<a name="using-cfn-updating-stacks-monitor-stack"></a>

You can monitor the progress of a stack update by viewing the stack's events\. The console's **Events** tab displays each major step in the creation and update of the stack sorted by the time of each event with latest events on top\. The start of the stack update process is marked with an UPDATE\_IN\_PROGRESS event for the stack:

```
2011-09-30 09:35 PDT AWS::CloudFormation::Stack MyStack UPDATE_IN_PROGRESS 
```

Next are events that mark the beginning and completion of the update of each resource that was changed in the update template\. For example, updating an [AWS::RDS::DBInstance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-rds-database-instance.html) resource named MyDB would result in the following entries:

```
2011-09-30 09:35 PDT AWS::RDS::DBInstance MyDB UPDATE_COMPLETE
2011-09-30 09:35 PDT AWS::RDS::DBInstance MyDB UPDATE_IN_PROGRESS
```

The UPDATE\_IN\_PROGRESS event is logged when AWS CloudFormation reports that it has begun to update the resource\. The UPDATE\_COMPLETE event is logged when the resource is successfully created\.

When AWS CloudFormation has successfully updated the stack, you will see the following event:

```
2011-09-30 09:35 PDT AWS::CloudFormation::Stack MyStack UPDATE_COMPLETE 
```

If an update of a resource fails, AWS CloudFormation reports an UPDATE\_FAILED event that includes a reason for the failure\. For example, if your update template specified a property change that is not supported by the resource such as reducing the size of AllocatedStorage for an [AWS::RDS::DBInstance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-rds-database-instance.html) resource, you would see events like these:

```
2011-09-30 09:36 PDT AWS::RDS::DBInstance MyDB UPDATE_FAILED Size cannot be less than current size; requested: 5; current: 10
2011-09-30 09:35 PDT AWS::RDS::DBInstance MyDB UPDATE_IN_PROGRESS
```

If a resource update fails, AWS CloudFormation rolls back any resources that it has updated during the upgrade to their configurations before the update\. Here is an example of the events you would see during an update rollback:

```
2011-09-30 09:38 PDT AWS::CloudFormation::Stack MyStack UPDATE_ROLLBACK_COMPLETE
2011-09-30 09:38 PDT AWS::RDS::DBInstance MyDB UPDATE_COMPLETE
2011-09-30 09:37 PDT AWS::RDS::DBInstance MyDB UPDATE_IN_PROGRESS
2011-09-30 09:37 PDT AWS::CloudFormation::Stack MyStack UPDATE_ROLLBACK_IN_PROGRESS The following resource(s) failed to update: [MyDB]
```

**Topics**
+ [To view stack events by using the console](#using-cfn-updating-stacks-monitor-stack.CON)
+ [To view stack events by using the command line](#using-cfn-updating-stacks-monitor-stack.CLI)

## To view stack events by using the console<a name="using-cfn-updating-stacks-monitor-stack.CON"></a>

1. In the [AWS CloudFormation console](https://console.aws.amazon.com/cloudformation), select the stack that you updated and then click the **Events** tab to view the stacks events\.

1. To update the event list with the most recent events, click the refresh button in the AWS CloudFormation console\.

## To view stack events by using the command line<a name="using-cfn-updating-stacks-monitor-stack.CLI"></a>
+ Use the command [https://docs.aws.amazon.com/cli/latest/reference/cloudformation/describe-stack-events.html](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/describe-stack-events.html) to view the events for a stack\.