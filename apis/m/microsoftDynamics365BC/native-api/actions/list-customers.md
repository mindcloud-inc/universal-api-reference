# List Customers with Microsoft Dynamics 365 BC

## Endpoint

- **Method:** `GET`
- **Path:** `https://api.businesscentral.dynamics.com/v2.0/{tenantId}/{environment}/api/v2.0/companies({{companyId}})/customers`
- **Base URL:** `https://api.businesscentral.dynamics.com/v2.0/{tenantId}/{environment}/api/ssi/aapi/`
- **API:** REST (Copy)
- **Official documentation:** [List Customers](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/api-reference/v2.0/api/dynamics_customer_get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | path | `list<string>` | no | The Id of the company. This Id can be find on the "Get Companies" Action |
| `$filter` | query | `string` | no | — |
| `displayName` | query | `string` | no | — |
