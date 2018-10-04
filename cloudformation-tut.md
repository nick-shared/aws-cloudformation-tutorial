
## the bible:
https://gitlab.com/cloudformation/tutorial
https://gitlab.com/cloudformation/tutorial/tree/master/step2
https://gitlab.com/cloudformation/tutorial/tree/master/step1

## to organize
https://theserverlessway.com/aws/cloudformation/templates/

## template design
http://awsbits.blogspot.com/2015/01/basic-cloudformation-template-design.html
http://awsbits.blogspot.com/2015/01/basic-cloudformation-template-design.html

https://medium.com/boltops/a-simple-introduction-to-aws-cloudformation-part-1-1694a41ae59d
https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/GettingStarted.Walkthrough.html
https://foxutech.com/aws-cloudformation-templates/
https://cloudacademy.com/blog/writing-your-first-cloudformation-template/
https://ig.nore.me/2014/08/the-first-babysteps-with-cloudformation/
http://cloudurable.com/tags/cloudformation-tutorial/index.html
https://blog.boltops.com/2018/02/14/aws-cloudformation-declarative-infrastructure-code-tutorial
https://sookocheff.com/post/aws/how-to-create-a-vpc-using-cloudformation/
https://sookocheff.com/post/aws/how-to-create-a-vpc-using-cloudformation/


## cloudformation limits
https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cloudformation-limits.html

## cloudformation best practices
https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/best-practices.html

## AWS SAM
https://github.com/awslabs/serverless-application-model

## Wrappers
troposphere
terraform
chalice
serverless
sparkleformation


## other interesting stuff
https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies_examples_ec2_instances-subnet.html
http://templates.cloudonaut.io/en/stable/vpc/


## AWS command line

validate/create a stack
aws cloudformation validate-template --template-body file://your-template.json
aws cloudformation create-stack --stack-name your-stack-name  --template-body file://your-template.json

## weird stuff about cloudformation
https://medium.com/@onclouds/aws-cloudformation-and-api-gateway-2de3ef858c0b


view stack
aws cloudformation list-stacks --profile demo
aws cloudformation describe-stack-events --stack-name babysteps --profile demo
aws cloudformation describe-stacks --stack-name babysteps --profile demo


update stack
aws cloudformation update-stack --stack-name babysteps --template-body file://cfn1-babysteps.json --profile demo
aws cloudformation delete-stack --stack-name babysteps --profile demo

command line resource
* https://ig.nore.me/2014/08/the-first-babysteps-with-cloudformation/
* https://blog.jayway.com/2016/08/17/introduction-to-cloudformation-for-api-gateway/

Note:
cloudformer does NOT work with API-Gateway and many other tools
