# Configuring CloudWatch Events for Systems Manager automation<a name="automation-cwe"></a>

You can configure Amazon CloudWatch Events to notify you of Systems Manager Automation events\. For example, you can configure CloudWatch Events to send notifications when an Automation step succeeds or fails\. You can also configure CloudWatch Events to send notifications if the Automation workflow succeeds or fails\. 

**Tip**  
For information about using the input transformer feature of Amazon CloudWatch Events to extract the `instance-id` of an EC2 instance from an instance state change event, see [Walkthrough: Using input transformers with Automation](automation-transformers.md)\.

Use the following procedure to configure CloudWatch Events to send notification about Automation events\.

**To configure CloudWatch Events for Automation**

1. Sign in to the AWS Management Console and open the CloudWatch console at [https://console\.aws\.amazon\.com/cloudwatch/](https://console.aws.amazon.com/cloudwatch/)\.

1. Choose **Events** in the left navigation, and then choose **Create rule**\.

1. Under **Event Source**, verify that **Event Pattern** is selected\.

1. In the **Service Name** field, choose **EC2 Simple Systems Manager \(SSM\)**

1. In the **Event Type** field, choose **Automation**\.

1. Choose the detail types and statuses for which you want to receive notifications\. For example, to select events for automations that fail choose **EC2 Automation Execution Status\-change Notification** and **Failed**\.

1. Choose **Add targets**\.

1. In the **Select target type** list, choose a target type\. For information about the different types of targets, see the corresponding AWS Help documentation\.

1. Choose **Configure details**\.

1. Specify the rule details, and then choose **Create rule**\.

The next time you run Automation, CloudWatch Events sends event details to the target you specified\.