# Terraform Module: Globals

This Terraform module provides a set of global resources and configurations that can be shared across multiple projects.

## Features

- Centralized configuration management
- Consistent resource naming conventions
- Standardized tagging and labeling
- Secure access control

## Usage

```hcl
module "globals" {
    source = "git::https://github.com/your-organization/terraform-modules//globals"

    region        = var.region
    environment   = var.environment
    project_name  = var.project_name
    vpc_cidr      = var.vpc_cidr
    subnet_cidrs  = var.subnet_cidrs
    ...
}
```

## Inputs

| Name          | Description                             | Type   | Default | Required |
|---------------|-----------------------------------------|--------|---------|----------|
| region        | The AWS region where resources are created | string | -       | yes      |
| environment   | The environment name                     | string | -       | yes      |
| project_name  | The name of the project                  | string | -       | yes      |
| vpc_cidr      | The CIDR block for the VPC               | string | -       | yes      |
| subnet_cidrs  | List of CIDR blocks for subnets          | list   | -       | yes      |
| ...           | ...                                     | ...    | ...     | ...      |

## Outputs

| Name          | Description                             |
|---------------|-----------------------------------------|
| vpc_id        | The ID of the VPC                        |
| subnet_ids    | List of subnet IDs                       |
| ...           | ...                                     |

## License

This module is licensed under the [MIT License](LICENSE).
