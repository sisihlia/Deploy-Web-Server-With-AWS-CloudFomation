# Deploy-Web-Server-With-AWS-CloudFormation
aws cloudformation create-stack --stack-name simpleInfra --template-body file://simpleInfra.yaml --parameters file://simpleInfra-params.json

aws cloudformation create-stack --stack-name simpleServer --template-body file://simpleServer.yaml --parameters file://simpleServer-params.json --capabilities "CAPABILITY_IAM" "CAPABILITY_NAMED_IAM"

Note: This is because we are creating an IAM Role to provide permissions and we want to make the person executing create-stack aware of this fact
