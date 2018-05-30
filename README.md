# aws-lambda-scheduled-function
Terraform module which created AWS API Method

These types of resources are created:
- aws_api_gateway_method
- aws_api_gateway_integration
- aws_api_gateway_method_response
- aws_api_gateway_integration_response
- aws_lambda_permission


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
  api_resource_path  = "${module.api.resource_path}"
}
````

License
-------
MIT
