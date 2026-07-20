# Create Credit Memo with Microsoft Dynamics 365 BC

## Endpoint

- **Method:** `POST`
- **Path:** `v2.0/companies(:company_id)/salesCreditMemos`
- **Base URL:** `https://api.businesscentral.dynamics.com/v2.0/{tenantId}/{environment}/api/`
- **API:** REST
- **Official documentation:** [Create Credit Memo](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/api-reference/v2.0/api/dynamics_customer_create)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `company_id` | path | `string` | yes |
| `customerNumber` | body | `string` | no |
| `externalDocumentNumber` | body | `string` | no |
| `creditMemoDate` | body | `string` | no |
| `postingDate` | body | `string` | no |
| `shortcutDimension1Code` | body | `string` | no |
| `shortcutDimension2Code` | body | `string` | no |
