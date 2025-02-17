# Overview

The idea behind comma is, to have a tool, that will analyze
the resources and their configurations in an AWS account and
find and identify those parts, that talk with each other.

# Identify Inputs

For example list all Lambda functions in an account and do
a check on all it's triggers to gain an overview which services
may send events to a particular lambda.

# Identify Outputs

Finding outputs will be a bit harder. But if a given Lambda
function has a VPC configuration, the security groups could
be checked if some RDS instance's security group has a reference
for the Lambda's security group.

Another way would be to investigate, if the Lambda's instance
role has permissions for writing objects into a S3 bucket or 
if the role contains permissions to write into a DynamoDB table.
