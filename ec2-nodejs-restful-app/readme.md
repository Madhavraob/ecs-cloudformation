aws cloudformation validate-template --template-body file://vpc-stack.yaml --profile madhav
aws cloudformation create-stack --stack-name vpcStack --template-body vpc-stack.yaml --profile madhav --capabilities CAPABILITY_IAM

aws cloudformation validate-template --template-body file://app-stack.yaml --profile madhav
aws cloudformation create-stack --stack-name ecsStack --template-body file://app-stack.yaml --profile madhav  --capabilities CAPABILITY_IAM
