# terraform-aws-acm-certificate

[![Release](https://img.shields.io/github/release/traveloka/terraform-aws-acm-certificate.svg)](https://github.com/traveloka/terraform-aws-acm-certificate/releases)
[![Last Commit](https://img.shields.io/github/last-commit/traveloka/terraform-aws-acm-certificate.svg)](https://github.com/traveloka/terraform-aws-acm-certificate/commits/master)
![Open Source Love](https://badges.frapsoft.com/os/v1/open-source.png?v=103)

## Description

Terraform module to create TLS/SSL certificate in Amazon Certificate Manager (ACM) using DNS validation by creating required Route53 validation record in the given Route53 hosted zone.

## Table of Content

- [Description](#Description)
- [Prerequisites](#Prerequisites)
- [Dependencies](#Dependencies)
- [Terraform Versions](#Terraform%20Versions)
- [Terraform Providers](#Terraform%20Providers)
- [Getting Started](#Getting_Started)
- [Inputs](#Inputs)
- [Outputs](#Outputs)
- [Contributing](#Contributing)
- [License](#License)
- [Acknowledgments](#Acknowledgments)

## Prerequisites

In order to provision this module, it is require some information from an existing resources as input parameter, those resources are:

- Route53 Zone, input variable that require the information from this resource are, `hosted_zone_name`

## Dependencies

Doesn't have any dependencies to any other Terraform module

## Terraform Versions

Created and tested using Terraform version `0.11.14`

## Terraform Providers

| Name   | Version |
| ------ | ------- |
| aws    | ~> 2.49 |

## Getting Started

<!-- BEGINNING OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:-----:|
| certificate\_name | Name of the ACM certificate. | `string` | n/a | yes |
| description | Free form description of this ACM certificate. | `string` | n/a | yes |
| domain\_name | Domain name the certificate is issued for. | `string` | n/a | yes |
| environment | Environment this ACM certificate belongs to. | `string` | n/a | yes |
| hosted\_zone\_name | Need for DNS validation, hosted zone name where record validation will be stored. | `string` | n/a | yes |
| product\_domain | Abbreviation of the product domain this ACM certificate belongs to. | `string` | n/a | yes |

## Outputs

| Name | Description |
|------|-------------|
| acm\_certificate\_arn | arn of acm certificate |
| acm\_certificate\_dns\_validation\_record | record which is used to validate acm certificate |

<!-- END OF PRE-COMMIT-TERRAFORM DOCS HOOK -->

## Contributing

This module accepting or open for any contributions from anyone, please see the [CONTRIBUTING.md](https://github.com/traveloka/terraform-aws-elasticache-memcached/blob/master/CONTRIBUTING.md) for more detail about how to contribute to this module.

## License

This module is under Apache License 2.0 - see the [LICENSE](https://github.com/traveloka/terraform-aws-elasticache-memcached/blob/master/LICENSE) file for details.