## Three foundational parts to an api-gateway

1> AWS::ApiGateway::RestApi
    * this is the main api
    * equivalent to create API button in the dash
2> AWS::ApiGateway::Resource
    * this is a path in the API
    * equivalent to create method option in dropdown in the dash
    * super simple
3> AWS::ApiGateway::Method
    * this is a method under the path
    * i.e. GET,POST,etc
    * equivalent to create method option in dropdown in the dash
    * complex


## Method Request
----
Authorization/Validations done here.


 When the validation fails, API Gateway immediately fails the request, returns a 400 error response to the caller, and publishes the validation results in CloudWatch Logs.

* https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-method.html#cfn-apigateway-method-integration

https://docs.aws.amazon.com/apigateway/api-reference/resource/method/

Requires a request validator resource
https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-requestvalidator.html



## Integration Request
---
Converts the request into a certain format/Passes the request to a backend
Sort of CGI, AWS style
Can literally remap anything including the HTTP verb

Theses are the flows that are possible. And all have unique configuration
 Lambda Function
    * straight shot to a lambda

 HTTP
    * can be used as a type of proxy to another site
    * basic mock via console


 Mock
    * a type of blank reponse, sends back a 200 but with not body in response
    * https://gorillalogic.com/blog/creating-mock-rest-service-within-api-gateway/
    * https://docs.aws.amazon.com/apigateway/latest/developerguide/how-to-mock-integration.html

 AWS Service
     * plugs API Gateway directly to another AWS servie

 VPC Link
    * not sure exacly, imaging it shoots the request inside of a VPC network

 Proxy
    * proxy to another link


https://docs.aws.amazon.com/apigateway/latest/developerguide/integration-request-basic-setup.html



## Integration Response
---
Recieves/modifies the response from backend to prepare to be sent back to the client
Note: Lambdas

https://docs.aws.amazon.com/apigateway/latest/developerguide/api-gateway-integration-settings-integration-response.html
https://docs.aws.amazon.com/apigateway/latest/developerguide/integration-passthrough-behaviors.html
https://docs.aws.amazon.com/apigateway/api-reference/resource/integration-response/

## Method Response
---
https://docs.aws.amazon.com/apigateway/latest/developerguide/api-gateway-method-settings-method-response.html


## Mapping
------
* https://sookocheff.com/post/api/understanding-api-gateway-payload-mappings/
* http://www.davekonopka.com/2016/api-gateway-models.html
* https://docs.aws.amazon.com/apigateway/latest/developerguide/request-response-data-mappings.html
* https://docs.aws.amazon.com/apigateway/latest/developerguide/models-mappings.html

---
IAM
Cogito


## validation
----
https://docs.aws.amazon.com/apigateway/latest/developerguide/api-gateway-request-validation-set-up.html


## using swagger
----
https://medium.com/@koxon/creating-a-public-api-description-part-3-33ec61ab65bb



## with lambdas integration
* two types of lambda integration
    * proxy- an event object is passed to the lambda, containing all of the parameters for the request in json object
    * non-proxy-nothing is passed to lambda. Basically a trigger.
* https://docs.aws.amazon.com/apigateway/latest/developerguide/set-up-lambda-proxy-integrations.html#api-gateway-simple-proxy-for-lambda-input-format

via console
https://blog.sourcerer.io/full-guide-to-developing-rest-apis-with-aws-api-gateway-and-aws-lambda-d254729d6992
http://www.davekonopka.com/2016/serverless-aws-lambda-api-gateway.html
https://medium.com/@lakshmanLD/lambda-proxy-vs-lambda-integration-in-aws-api-gateway-3a9397af0e6d
https://cloudacademy.com/course/build-aws-serverless-web-applications-with-python/setting-up-the-services-1/
https://forums.aws.amazon.com/thread.jspa?threadID=240734

aws docs
https://docs.aws.amazon.com/apigateway/latest/developerguide/integrating-api-with-aws-services-lambda.html
https://docs.aws.amazon.com/step-functions/latest/dg/tutorial-lambda-state-machine-cloudformation.html
https://docs.aws.amazon.com/apigateway/latest/developerguide/getting-started-lambda-non-proxy-integration.html


cloudformation resources
https://cloudonaut.io/create-a-serverless-restful-api-with-api-gateway-cloudformation-lambda-and-dynamodb/
https://blog.jayway.com/2016/08/17/introduction-to-cloudformation-for-api-gateway/
https://auth0.com/docs/integrations/aws-api-gateway/custom-authorizers/part-1


using troposphere
https://mysteriouscode.io/blog/deploying-apigateway-and-lambda-with-cloudformation/

examples
https://gist.github.com/magnetikonline/c314952045eee8e8375b82bc7ec68e88
https://github.com/MysteriousCode/cloudformation-examples/blob/master/templates/apigateway_with_lambda.json




## with AWS integration
https://docs.aws.amazon.com/apigateway/latest/developerguide/getting-started-aws-proxy.html
https://blog.powerupcloud.com/api-gateway-part-ii-aws-api-gateway-with-private-integration-2545e8d70395

## with proxy integration
https://cjohansen.no/aws-apigw-proxy-cloudformation/


## IAM and api gateway
https://docs.aws.amazon.com/apigateway/latest/developerguide/api-gateway-iam-policy-examples.html

## books/papers
https://www.amazon.com/dp/1787129195/?tag=stackoverflow17-20
https://d1.awsstatic.com/whitepapers/serverless-architectures-with-aws-lambda.pdf
https://www.contino.io/files/Contino-Introduction-to-Serverless-Computing-with-AWS-Lambda.pdf
https://manning-content.s3.amazonaws.com/download/c/ec3adab-f277-4512-9de7-e166b9d2bd3b/SampleCh01.pdf
https://www.usenix.org/system/files/conference/hotcloud18/hotcloud18-paper-hong.pdf
https://www.manning.com/books/amazon-web-services-in-action?a_bid=65e87b33&a_aid=mwittig
aws in action:
    https://s3-ap-southeast-1.amazonaws.com/tv-prod/documents%2Fnull-Amazon+Web+Services+in+Action.pdf
    https://github.com/AWSinAction/code


## api gateway error handling
https://blog.jayway.com/2015/11/07/error-handling-in-api-gateway-and-aws-lambda/


## general stuff
https://docs.aws.amazon.com/apigateway/latest/developerguide/api-gateway-tutorials.html
https://serverlesscode.com/post/cloudformation-deploy-lambda-resources/
https://brightinventions.pl/blog/deploy-lambda-with-cloudformation/
http://derpturkey.com/a-simple-aws-cloudformation-example-with-lambda-and-kinesis/