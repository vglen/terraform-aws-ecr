## Requirements

| Name | Version |
|------|---------|
| <a name="requirement_terraform"></a> [terraform](#requirement\_terraform) | >= 0.15.5 |
| <a name="requirement_aws"></a> [aws](#requirement\_aws) | >= 3.45.0 |

## Providers

| Name | Version |
|------|---------|
| <a name="provider_aws"></a> [aws](#provider\_aws) | >= 3.45.0 |

## Modules

No modules.

## Resources

| Name | Type |
|------|------|
| [aws_ecr_lifecycle_policy.repo_lifecycle](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/ecr_lifecycle_policy) | resource |
| [aws_ecr_repository.repo](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/ecr_repository) | resource |
| [aws_ecr_repository_policy.policy](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/ecr_repository_policy) | resource |
| [aws_iam_policy_document.repo_policy](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/data-sources/iam_policy_document) | data source |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_enable_kms"></a> [enable\_kms](#input\_enable\_kms) | True for KMS, false for AES256 | `bool` | `false` | no |
| <a name="input_encryption_type"></a> [encryption\_type](#input\_encryption\_type) | Type of encryption for the repository | `string` | `"AES256"` | no |
| <a name="input_kms_key_arn"></a> [kms\_key\_arn](#input\_kms\_key\_arn) | The arn of the kms key is not using default of AES256 | `string` | `""` | no |
| <a name="input_life_cycle_policy_days"></a> [life\_cycle\_policy\_days](#input\_life\_cycle\_policy\_days) | The humber of days to hold untagged images | `number` | `90` | no |
| <a name="input_life_cycle_policy_tagstatus"></a> [life\_cycle\_policy\_tagstatus](#input\_life\_cycle\_policy\_tagstatus) | The status of the image tag | `string` | `"untagged"` | no |
| <a name="input_principals_pull_access"></a> [principals\_pull\_access](#input\_principals\_pull\_access) | Principal ARNs to provide with pull access to the ECR | `list(string)` | `[]` | no |
| <a name="input_repo_name"></a> [repo\_name](#input\_repo\_name) | Name of your ECR Repo | `any` | n/a | yes |
| <a name="input_scan_on_push"></a> [scan\_on\_push](#input\_scan\_on\_push) | Enable vulnerability scanning on ECR repo | `bool` | `true` | no |

## Outputs

| Name | Description |
|------|-------------|
| <a name="output_repo"></a> [repo](#output\_repo) | n/a |