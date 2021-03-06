# AWS::EC2::LaunchTemplate TagSpecification<a name="aws-properties-ec2-launchtemplate-tagspecification"></a>

Specifies tags to apply to a resource when the resource is created\.

 `TagSpecification` is a property type of the [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-launchtemplate-launchtemplatedata.html#cfn-ec2-launchtemplate-launchtemplatedata-tagspecifications](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-launchtemplate-launchtemplatedata.html#cfn-ec2-launchtemplate-launchtemplatedata-tagspecifications) property\. [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-launchtemplate-launchtemplatedata.html#cfn-ec2-launchtemplate-launchtemplatedata-tagspecifications](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-launchtemplate-launchtemplatedata.html#cfn-ec2-launchtemplate-launchtemplatedata-tagspecifications) is a property of the [Amazon EC2 LaunchTemplate LaunchTemplateData](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-launchtemplate-launchtemplatedata.html) property type\.

## Syntax<a name="aws-properties-ec2-launchtemplate-tagspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-launchtemplate-tagspecification-syntax.json"></a>

```
{
  "[ResourceType](#cfn-ec2-launchtemplate-tagspecification-resourcetype)" : String,
  "[Tags](#cfn-ec2-launchtemplate-tagspecification-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
}
```

### YAML<a name="aws-properties-ec2-launchtemplate-tagspecification-syntax.yaml"></a>

```
  [ResourceType](#cfn-ec2-launchtemplate-tagspecification-resourcetype): String
  [Tags](#cfn-ec2-launchtemplate-tagspecification-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-properties-ec2-launchtemplate-tagspecification-properties"></a>

`ResourceType`  <a name="cfn-ec2-launchtemplate-tagspecification-resourcetype"></a>
The type of resource to tag\.  
*Required*: No  
*Type*: String  
*Allowed Values*: `client-vpn-endpoint | customer-gateway | dedicated-host | dhcp-options | elastic-ip | fleet | fpga-image | host-reservation | image | instance | internet-gateway | key-pair | launch-template | natgateway | network-acl | network-interface | placement-group | reserved-instances | route-table | security-group | snapshot | spot-fleet-request | spot-instances-request | subnet | traffic-mirror-filter | traffic-mirror-session | traffic-mirror-target | transit-gateway | transit-gateway-attachment | transit-gateway-multicast-domain | transit-gateway-route-table | volume | vpc | vpc-flow-log | vpc-peering-connection | vpn-connection | vpn-gateway`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-ec2-launchtemplate-tagspecification-tags"></a>
The tags to apply to the resource\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See Also<a name="aws-properties-ec2-launchtemplate-tagspecification--seealso"></a>
+  [ LaunchTemplateTagSpecificationRequest](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_LaunchTemplateTagSpecificationRequest.html) in the *Amazon Elastic Compute Cloud API Reference* 