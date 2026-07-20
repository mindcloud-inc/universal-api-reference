# Delete Tenant with Acronis

Deletes an existing tenant from Acronis.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/2/tenants/{tenant_id}`
- **Base URL:** `{dataCenterUrl}`
- **Official documentation:** [Delete Tenant](https://developer.acronis.com/doc/outbound/apis/api-library/account/tenants/deleting-tenant.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tenant_id` | path | `string` | yes | Tenant Id path parameter. |
