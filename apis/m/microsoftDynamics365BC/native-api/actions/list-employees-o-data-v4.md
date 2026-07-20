# List Employees ODataV4 with Microsoft Dynamics 365 BC

## Endpoint

- **Method:** `GET`
- **Path:** `https://api.businesscentral.dynamics.com/v2.0/{tenantId}/{environment}/ODataV4/Company(:companyId)/GravityResources`
- **Base URL:** `https://api.businesscentral.dynamics.com/v2.0/{tenantId}/{environment}/api/`
- **API:** REST
- **Official documentation:** [List Employees ODataV4](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/api-reference/v2.0/api/dynamics_customer_get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | path | `list<string>` | no | The Id of the company. This Id can be find on the "Get Companies" Action Accepted values: `'Esser%20Plumbing%20%26%20Heating'`. |
| `$filter` | query | `string` | no | — |
