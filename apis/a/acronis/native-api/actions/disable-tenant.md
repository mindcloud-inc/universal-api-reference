# Disable Tenant with Acronis

Disables an existing tenant in Acronis.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/2/tenants/{tenant_id}`
- **Base URL:** `{dataCenterUrl}`
- **Official documentation:** [Disable Tenant](https://developer.acronis.com/doc/outbound/apis/api-library/account/tenants/disabling-tenant.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tenant_id` | path | `string` | yes | Tenant Id path parameter. |
