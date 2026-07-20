# Update Tenant with Frontegg

Updates an existing account in Frontegg.

## Endpoint

- **Method:** `PUT`
- **Path:** `/tenants/resources/tenants/v2/:tenantId`
- **Base URL:** `https://api.frontegg.com`
- **Official documentation:** [Update Tenant](https://developers.frontegg.com/ciam/api/tenants/accounts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tenantId` | path | `string` | yes | The tenant ID to update. |
| `name` | body | `string` | no | Updated tenant name. |
