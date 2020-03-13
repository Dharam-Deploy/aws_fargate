# AWS FARGATE DEPLOYMENT USING CIRCLECI WITH DOCKER FLASK IMAGE
The Docker Image will provide an REST API to store objects in bucket which will take credentials and bucket_name as an input and provides storing objects while temporary storing the object(intermediate processing). 

### Configure environment variables on CircleCI
The following must be set for the project on CircleCI via the project settings page, before the project can be built successfully.


| Variable                       | Description                                               |
| ------------------------------ | --------------------------------------------------------- |
| `AWS_ACCESS_KEY_ID`            | Used by the AWS CLI                                       |
| `AWS_SECRET_ACCESS_KEY `       | Used by the AWS CLI                                       |
| `AWS_DEFAULT_REGION`           | Used by the AWS CLI. Example value: "us-east-1" (Please make sure the specified region is supported by the Fargate launch type)                          |
| `AWS_ACCOUNT_ID`               | AWS account id. This information is required for deployment.                                   |
| `AWS_RESOURCE_NAME_PREFIX`     | Prefix that some of the required AWS resources are assumed to have in their names.