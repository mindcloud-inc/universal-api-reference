# List Journal Line with Microsoft Dynamics 365 BC

## Endpoint

- **Method:** `GET`
- **Path:** `v2.0/companies(:company_id)/journals(:journal_id)/journalLines`
- **Base URL:** `https://api.businesscentral.dynamics.com/v2.0/{tenantId}/{environment}/api/`
- **API:** REST
- **Official documentation:** [List Journal Line](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/api-reference/v2.0/api/dynamics_salesorder_get)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `company_id` | path | `list` | no |
| `$filter` | query | `string` | no |
| `journal_id` | path | `string` | no |
