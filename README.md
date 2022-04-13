# Terraform-Kubernetes-App
## Example
```hcl
module "simple_webapp" {
  source = "app.terraform.io/VeloCloud-Terraform/app/kubernetes"
  version = "x.x.x"
  image = "training/webapp"
  name = "simple-webapp"

  container_port = 5000
  replicas = 2

  env_vars = {
    PROVIDER = "Terraform"
  }
}
```
## Resources
| Name | Type |
|------|------|
| [kubernetes_deployment](https://registry.terraform.io/providers/hashicorp/kubernetes/latest/docs/resources/deployment) | resource |
| [kubernetes_service](https://registry.terraform.io/providers/hashicorp/kubernetes/latest/docs/resources/service) | resource |