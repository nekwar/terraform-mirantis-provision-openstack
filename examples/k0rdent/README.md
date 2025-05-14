# TF chart to deploy k0rdent on Openstack

## Usage

1. Copy `terraform.tfvars.example` to `terraform.tfvars` and put variables there according to your environment and needs
2. Execute `terraform init`
3. Execute `terraform apply`
4. To provision k0rdent cluster, run `terraform output -raw k0s_cluster | k0sctl apply --config -`
5. To get kubeconfig for created cluster, run `terraform output -raw k0s_cluster | k0sctl kubeconfig --config -`
