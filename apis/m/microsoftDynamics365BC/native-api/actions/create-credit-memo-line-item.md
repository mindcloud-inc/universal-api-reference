# Create Credit Memo Line Item with Microsoft Dynamics 365 BC

## Endpoint

- **Method:** `POST`
- **Path:** `v2.0/companies(:company_id)/salesCreditMemos(:creditMemoId)/salesCreditMemoLines`
- **Base URL:** `https://api.businesscentral.dynamics.com/v2.0/{tenantId}/{environment}/api/`
- **API:** REST
- **Official documentation:** [Create Credit Memo Line Item](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/api-reference/v2.0/api/dynamics_customer_create)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `company_id` | path | `string` | yes |
| `lineType` | body | `string` | no |
| `lineObjectNumber` | body | `string` | no |
| `description` | body | `string` | no |
| `unitPrice` | body | `number` | no |
| `quantity` | body | `number` | no |
| `creditMemoId` | path | `string` | no |
| `taxCode` | body | `string` | no |
| `taxAreaCode` | body | `string` | no |
