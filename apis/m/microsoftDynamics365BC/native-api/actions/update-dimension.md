# Update Dimension with Microsoft Dynamics 365 BC

## Endpoint

- **Method:** `PATCH`
- **Path:** `v2.0/companies({{companyId}})/dimensionValues({{dimensionId}})`
- **Base URL:** `https://api.businesscentral.dynamics.com/v2.0/{tenantId}/{environment}/api/`
- **API:** REST
- **Official documentation:** [Update Dimension](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/api-reference/v2.0/api/dynamics_customer_get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | path | `list<string>` | no | The Id of the company. This Id can be find on the "Get Companies" Action |
| `dimensionId` | path | `string` | no | — |
| `displayName` | body | `string` | no | — |
