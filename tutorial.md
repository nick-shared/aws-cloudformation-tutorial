Prerequisites
Understanding how the console API Gateway works
    * this is important because the Cloudformation has alot in common from a mechanical perspective
    * It's highly suggested to build a few test RestApi's with the console to see how things work from a mechanical perspective
    * Follow this tutorial to build a simple mock endpoint
    * https://gorillalogic.com/blog/creating-mock-rest-service-within-api-gateway/

Good understanding of the structure of an HTTP request
        * Everything is based around fields in the HTTP Request
        * http://www.ntu.edu.sg/home/ehchua/programming/webprogramming/http_basics.html

Understanding of Cloudformation template structure
        


Data from API Gateway to Lambda
The data payload will arrive in the Lambda as the event object

Input format:
https://docs.aws.amazon.com/apigateway/latest/developerguide/set-up-lambda-proxy-integrations.html#api-gateway-simple-proxy-for-lambda-input-format