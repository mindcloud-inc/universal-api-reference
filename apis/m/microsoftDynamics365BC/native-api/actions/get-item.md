# Get Item with Microsoft Dynamics 365 BC

## Endpoint

- **Method:** `GET`
- **Path:** `v2.0/companies(:companyId)/items(:itemId)`
- **Base URL:** `https://api.businesscentral.dynamics.com/v2.0/{tenantId}/{environment}/api/`
- **API:** REST
- **Official documentation:** [Get Item](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/api-reference/v2.0/api/dynamics_item_get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | path | `list<string>` | yes | The Business Central company that holds the item. |
| `itemId` | path | `string` | yes | The item's system ID (GUID), not the item number. |
