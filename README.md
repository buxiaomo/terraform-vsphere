# how to use

1. create tfvars file
2. terraform init
3. terraform apply

example:
```
terraform init \
-backend-config "endpoint=http://172.16.1.10:9000" \
-backend-config "access_key=minioadmin" \
-backend-config "secret_key=minioadmin" \
-backend-config "bucket=terraform" \
-backend-config "key=zabbix.tfstate"

terraform apply -auto-approve -no-color -var-file=auth.tfvars -var-file=./instance/zabbix.tfvars
```