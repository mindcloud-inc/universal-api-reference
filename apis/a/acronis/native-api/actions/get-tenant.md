# Get Tenant with Acronis

Retrieves a tenant from Acronis.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/2/tenants/{tenant_id}`
- **Base URL:** `{dataCenterUrl}`
- **Official documentation:** [Get Tenant](https://developer.acronis.com/doc/outbound/apis/api-library/account/tenants/fetching-tenant.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tenant_id` | path | `string` | yes | Tenant Id path parameter. |
