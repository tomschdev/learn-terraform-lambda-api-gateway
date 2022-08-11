# Learn Terraform - Lambda functions and API Gateway

AWS Lambda functions and API gateway are often used to create serverlesss
applications.

Follow along with this [tutorial on HashiCorp

Learn](https://learn.hashicorp.com/tutorials/terraform/lambda-api-gateway?in=terraform/aws).

The source files have been modified according to the tutorial. \
By applying the deployment, a lamda handler and api-gateway will be provisioned. \
The gateway accepts a GET request at <base\_url>/hello. \
The base\_url is outputted in the terminal after deployment. 

## Exectuion

```bash
cd <root>
terraform apply

```
You will be prompted to enter 'yes' to apply changes to aws resources. \
The API should now be exposed. \
Test the endpoint:
```bash
curl "$(terraform output -raw base_url)/hello?Name=tomschdev"
```


