# Deploy-Web-Server-With-AWS-CloudFormation

In this project, you’ll deploy web servers for a highly available web app using CloudFormation. You will write the code that creates and deploys the infrastructure and application for an Instagram-like app from the ground up. You will begin with deploying the networking components, followed by servers, security roles and software. The procedure you follow here will become part of your portfolio of cloud projects. You’ll do it exactly as it’s done on the job - following best practices and scripting as much as possible. 

aws cloudformation create-stack --stack-name simpleInfra --template-body file://simpleInfra.yaml --parameters file://simpleInfra-params.json

aws cloudformation create-stack --stack-name simpleServer --template-body file://simpleServer.yaml --parameters file://simpleServer-params.json --capabilities "CAPABILITY_IAM" "CAPABILITY_NAMED_IAM"

Note: This is because we are creating an IAM Role to provide permissions and we want to make the person executing create-stack aware of this fact
