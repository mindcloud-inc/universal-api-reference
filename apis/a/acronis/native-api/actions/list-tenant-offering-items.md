# List Tenant Offering Items with Acronis

Retrieves available offering items for a tenant in Acronis.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/2/tenants/{tenant_id}/offering_items`
- **Base URL:** `{dataCenterUrl}`
- **Official documentation:** [List Tenant Offering Items](https://developer.acronis.com/doc/outbound/apis/api-library/account/offering-items/fetching-available-ois.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tenant_id` | path | `string` | yes | Tenant Id path parameter. |
