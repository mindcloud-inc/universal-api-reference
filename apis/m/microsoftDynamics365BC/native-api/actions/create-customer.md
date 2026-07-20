# Create Customer with Microsoft Dynamics 365 BC

## Endpoint

- **Method:** `POST`
- **Path:** `v2.0/companies(:company_id)/customers`
- **Base URL:** `https://api.businesscentral.dynamics.com/v2.0/{tenantId}/{environment}/api/`
- **API:** REST
- **Official documentation:** [Create Customer](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/api-reference/v2.0/api/dynamics_customer_create)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `company_id` | path | `string` | yes |
| `displayName` | body | `string` | no |
| `type` | body | `string` | no |
| `addressLine1` | body | `string` | no |
| `addressLine2` | body | `string` | no |
| `phoneNumber` | body | `string` | no |
| `email` | body | `string` | no |
| `city` | body | `string` | no |
| `state` | body | `string` | no |
| `country` | body | `string` | no |
| `postalCode` | body | `string` | no |
| `website` | body | `string` | no |
