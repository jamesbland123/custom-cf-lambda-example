# Example custom resource for CloudFormation

> This is meant to be a toy example to show how to use crhelper and lambda to create a custom
> resource for CloudFormation.

```
cd lambda
pip install -t . crhelper
```

Zip up your function
```
zip -r ../../sum.zip ./

```

Create a Lambda function with python 3.7.  

Edit sum.yaml and change the function arn to the actual lambda ARN


Run the following in the aws cli and create a stack.  Check the output and the result of the sum should be there.

```
aws cloudformation create-stack --stack-name sumtest --template-body file://sum.yaml --region us-west-2
```