# Azure Landing Zones Terraform Accelerator Example (US SLED)

This repository contains a full, practical example for deploying Azure Landing Zones with the Azure Verified Modules (AVM) ALZ accelerator patterns.

The example is built to show end-to-end configuration across platform areas such as:

- Management group hierarchy and policy configuration
- Management resources and AMBA integration
- Hub-and-spoke networking
- Optional connectivity paths (ExpressRoute and VPN)
- Optional shared services (Firewall, Bastion, DDoS protection, DNS)

## Repository layout

- `/examples/hub-and-spoke` – primary in-depth example
  - `terraform.tfvars` – main configuration with guided placeholders and notes
  - `README.md` – example-specific usage details

## How to use this repository

1. Review `/examples/hub-and-spoke/README.md` for the execution flow.
2. Copy and update `/examples/hub-and-spoke/terraform.tfvars` values marked `TO-BE-UPDATED`.
3. Use the note blocks in `terraform.tfvars` to locate feature-specific configuration quickly.

## Finding where to configure specific capabilities

`/examples/hub-and-spoke/terraform.tfvars` includes labeled comments that point to feature areas. Search for these markers:

- `EXPRESS ROUTE NOTE`
- `VPN NOTE`
- `EXPRESS ROUTE & VPN NOTE`
- `AZURE FIREWALL NOTE`
- `BASTION NOTE`
- `DDOS PROTECTION NOTE`
- `MULTI-REGION NOTE`

These markers identify where to adjust placeholders and settings for each capability.

## Contributing

This project welcomes contributions and suggestions. Most contributions require you to agree to a Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us the rights to use your contribution. For details, visit [Contributor License Agreements](https://cla.opensource.microsoft.com).

When you submit a pull request, a CLA bot will automatically determine whether you need to provide a CLA and decorate the PR appropriately (for example, status check or comment). Follow the instructions provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/). For more information, see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

## Trademarks

This project may contain trademarks or logos for projects, products, or services. Authorized use of Microsoft trademarks or logos is subject to and must follow [Microsoft's Trademark & Brand Guidelines](https://www.microsoft.com/legal/intellectualproperty/trademarks/usage/general). Use of Microsoft trademarks or logos in modified versions of this project must not cause confusion or imply Microsoft sponsorship. Any use of third-party trademarks or logos is subject to those third-party's policies.
