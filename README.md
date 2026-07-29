# Azure Landing Zones Terraform Accelerator Example (US SLED)

This repository **is** a full, in-depth example of deploying Azure Landing Zones using the [Azure Verified Modules (AVM) ALZ Terraform accelerator](https://aka.ms/alz/acc). It demonstrates a complete platform landing zone deployment covering:

- Management group hierarchy and policy assignments
- Management resources (Log Analytics, Automation Account, data collection rules)
- Azure Monitor Baseline Alerts (AMBA) integration
- Hub-and-spoke virtual network connectivity

## Getting started

### Required values

Every value marked `TO-BE-UPDATED` in `terraform.tfvars` **must** be replaced before running Terraform. These include:

- Subscription IDs for connectivity, identity, management, and security subscriptions
- Azure region(s) (`starter_locations`)
- Root parent management group ID
- Default management group name

Search the file for `TO-BE-UPDATED` to find every required value.

### Running the deployment

1. Review [`examples/hub-and-spoke/README.md`](./examples/hub-and-spoke/README.md) for execution steps.
2. Replace all `TO-BE-UPDATED` values in `terraform.tfvars`.
3. Run `terraform init` and `terraform apply -var-file ./examples/hub-and-spoke/terraform.tfvars`.

## Finding service-specific configuration

Throughout `terraform.tfvars`, comment blocks use the pattern `# <SERVICE> NOTE:` to mark every location where a given service is configured. Search for any of the tags below to find all relevant settings for that capability:

| Comment marker | Where it appears |
|---|---|
| `# EXPRESS ROUTE NOTE:` | ExpressRoute gateway name, SKU, circuit ID, and connection settings |
| `# VPN NOTE:` | VPN gateway name, SKU, public IPs, local network gateway, and connection settings |
| `# EXPRESS ROUTE & VPN NOTE:` | Shared gateway subnet route table used by both gateway types |
| `# AZURE FIREWALL NOTE:` | Azure Firewall name, SKU, subnet sizing, and UDR configuration |
| `# AZURE FIREWALL POLICY NOTE:` | Firewall policy base policy inheritance and rule override settings |
| `# AZURE FIREWALL NVA NOTE:` | Third-party NVA name variables and hub router IP |
| `# HUB NVA NOTE:` | NVA hub router IP used in spoke UDR next-hop settings |
| `# BASTION NOTE:` | Azure Bastion host name, public IP, and subnet settings |
| `# DDOS PROTECTION NOTE:` | DDoS Protection Plan name, ID reference, and enforcement mode |
| `# ROUTE TABLE NOTE:` | Route table names and firewall route references |
| `# MULTI-REGION NOTE:` | Secondary region hub, spoke, and cross-region routing settings |

## Contributing

This project welcomes contributions and suggestions. Most contributions require you to agree to a Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us the rights to use your contribution. For details, visit [Contributor License Agreements](https://cla.opensource.microsoft.com).

When you submit a pull request, a CLA bot will automatically determine whether you need to provide a CLA and decorate the PR appropriately (for example, status check or comment). Follow the instructions provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/). For more information, see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

## Trademarks

This project may contain trademarks or logos for projects, products, or services. Authorized use of Microsoft trademarks or logos is subject to and must follow [Microsoft's Trademark & Brand Guidelines](https://www.microsoft.com/legal/intellectualproperty/trademarks/usage/general). Use of Microsoft trademarks or logos in modified versions of this project must not cause confusion or imply Microsoft sponsorship. Any use of third-party trademarks or logos is subject to those third-party's policies.
