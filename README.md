# Terraform-Kubernetes-App
## Example
```hcl
module "simple_webapp" {
  source = "app.terraform.io/VeloCloud-Terraform/terraform-kubernetes-app/kubernets"
  image = "training/webapp"
  name = "simple-webapp"

  container_port = 5000
  replicas = 2

  env_vars = {
    PROVIDER = "Terraform"
  }
}
```