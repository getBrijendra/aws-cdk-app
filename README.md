# Welcome to your CDK JavaScript project

This is a blank project for CDK development with JavaScript.

The `cdk.json` file tells the CDK Toolkit how to execute your app. The build step is not required when using JavaScript.

## Useful commands

- `npm run test` perform the jest unit tests
- `cdk deploy` deploy this stack to your default AWS account/region
- `cdk diff` compare deployed stack with current state
- `cdk synth` emits the synthesized CloudFormation template

### ----------------------------

# 1. install the CDK

sudo npm install -g aws-cdk@2

# directory name must be cdk-app/ to go with the rest of the tutorial, changing it will cause an error

mkdir cdk-app
cd cdk-app/

# initialize the application

npx aws-cdk@2.x init app --language javascript

# verify it works correctly

cdk ls

# install the necessary packages

[Not needed]
npm install @aws-cdk/aws-s3 @aws-cdk/aws-iam @aws-cdk/aws-lambda @aws-cdk/aws-lambda-event-sources @aws-cdk/aws-dynamodb
npm install aws-cdk-lib

# 2. copy the content of cdk-app-stack.js into lib/cdk-app-stack.js

# 3. setup the Lambda function

mkdir lambda && touch index.py

# 4. bootstrap the CDK application

cdk bootstrap

# 5. (optional) synthesize as a CloudFormation template

cdk synth

# 6. deploy the CDK stack

cdk deploy

# 7. empty the s3 bucket

# 8. destroy the stack

cdk destroy
