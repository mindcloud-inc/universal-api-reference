# Get Tenant Production Start Date with Acronis

Retrieves a tenant's production start date from Acronis.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/2/tenants/{tenant_id}/pricing`
- **Base URL:** `{dataCenterUrl}`
- **Official documentation:** [Get Tenant Production Start Date](https://developer.acronis.com/doc/outbound/apis/api-library/account/tenants/fetching-tenant-prod-date.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tenant_id` | path | `string` | yes | Tenant Id path parameter. |
