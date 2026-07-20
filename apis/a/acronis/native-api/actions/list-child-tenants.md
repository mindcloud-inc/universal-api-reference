# List Child Tenants with Acronis

Retrieves child tenants for a tenant in Acronis.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/2/tenants/{tenant_id}/children`
- **Base URL:** `{dataCenterUrl}`
- **Official documentation:** [List Child Tenants](https://developer.acronis.com/doc/outbound/apis/api-library/account/tenants/fetching-child-tenants.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tenant_id` | path | `string` | yes | Tenant Id path parameter. |
