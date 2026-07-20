# Update Costumer SSI with Microsoft Dynamics 365 BC

## Endpoint

- **Method:** `PATCH`
- **Path:** `v2.0/companies(:companyId)/customersSSI(:customerId)`
- **Base URL:** `https://api.businesscentral.dynamics.com/v2.0/{tenantId}/{environment}/api/ssi/aapi/`
- **API:** REST (Copy)
- **Official documentation:** [Update Costumer SSI](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/api-reference/v2.0/api/dynamics_customer_update)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `city` | body | `string` | no |
| `documentSendingProfile` | body | `string` | no |
| `no` | body | `string` | no |
| `address` | body | `string` | no |
| `postCode` | body | `string` | no |
| `county` | body | `string` | no |
| `salespersonCode` | body | `string` | no |
| `name` | body | `string` | no |
| `salesforceCustomerNo` | body | `string` | no |
| `companyId` | path | `string` | yes |
| `customerId` | path | `string` | yes |
| `email` | body | `string` | no |
