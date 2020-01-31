# terraform-aws-acm-certificate

[![Terraform Version](https://img.shields.io/badge/Terraform%20Version->=0.11.14,_<0.12.0-blue.svg)](https://releases.hashicorp.com/terraform/)
[![Release](https://img.shields.io/github/release/traveloka/terraform-aws-acm-certificate.svg)](https://github.com/traveloka/terraform-aws-acm-certificate/releases)
[![Last Commit](https://img.shields.io/github/last-commit/traveloka/terraform-aws-acm-certificate.svg)](https://github.com/traveloka/terraform-aws-acm-certificate/commits/master)
[![Issues](https://img.shields.io/github/issues/traveloka/terraform-aws-acm-certificate.svg)](https://github.com/traveloka/terraform-aws-acm-certificate/issues)
[![Pull Requests](https://img.shields.io/github/issues-pr/traveloka/terraform-aws-acm-certificate.svg)](https://github.com/traveloka/terraform-aws-acm-certificate/pulls)
[![License](https://img.shields.io/github/license/traveloka/terraform-aws-acm-certificate.svg)](https://github.com/traveloka/terraform-aws-acm-certificate/blob/master/LICENSE)
![Open Source Love](https://badges.frapsoft.com/os/v1/open-source.png?v=103)

## Table of Content

- [Prerequisites](#Prerequisites)
- [Quick Start](#Quick-Start)
- [Dependencies](#Dependencies)
- [Contributing](#Contributing)
- [Contributor](#Contributor)
- [License](#License)
- [Acknowledgments](#Acknowledgments)

## Prerequisites

- [Terraform](https://releases.hashicorp.com/terraform/). This module currently tested on `0.11.14`

## Quick Start
This Terraform module creates TLS/SSL certificate in Amazon Certificate Manager (ACM), and validates it with DNS by creating required Route 53 validation record in the given Route 53 hosted zone.

### Examples

* [DNS Validation](https://github.com/traveloka/terraform-aws-acm-certificate/tree/master/examples/dns_validation)

## Providers

| Name | Version |
|------|---------|
| aws | n/a |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:-----:|
| certificate_name | Name of the ACM certificate. | `string` | n/a | yes |
| product\_domain | Product domain these resources belong to. | `string` | n/a | yes |
| environment | Type of environment these resources belong to. | `string` | n/a | yes |
| description | Description of what this bucket used for. | `string` | n/a | yes |
| domain_name | Domain name the certificate is issued for. | `string` | n/a | yes |
| hosted_zone_name | Need for DNS validation, hosted zone name where record validation will be stored. | `string` | `private` | yes |

## Outputs

| Name | Description |
|------|-------------|
| acm_certificate_arn | ARN of ACM certificate. |
| acm_certificate_dns_validation_record | Record which is used to validate ACM certificate. |

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md)

## License

Apache 2 Licensed. See LICENSE for full details.
