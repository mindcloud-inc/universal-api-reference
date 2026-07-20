# Toggle Tenant Offering Item with Acronis

Enables or disables a tenant offering item in Acronis.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/2/tenants/{tenant_id}/offering_items`
- **Base URL:** `{dataCenterUrl}`
- **Official documentation:** [Toggle Tenant Offering Item](https://developer.acronis.com/doc/outbound/apis/api-library/account/offering-items/enabling-disabling-ois.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tenant_id` | path | `string` | yes | Tenant Id path parameter. |
