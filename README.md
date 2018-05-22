# aws-lambda-scheduled-function
Terraform module which created AWS API Method

These types of resources are created:
- ...

Lambda function role is not created by default, it has to be pass as parameter to the module

Usage
-------
````

module "ec2manager_api_method_get" {
  source             = "birkoff/api-method"
  region             = "eu-central-1"
  api_id             = "${module.api.id}"
  integration_type   = "AWS_PROXY"
  http_method        = "GET"
  lambda_fuction_arn = "${module.lambda.lamda_fuction_arn}"
  api_resource_id    = "${module.api.resource_id}"
  authorization      = "NONE"
}
````

License
-------
MIT
