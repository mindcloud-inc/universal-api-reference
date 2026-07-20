# Switch Tenant Service Edition with Acronis

Switches a tenant service edition in Acronis.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/2/tenants/{tenant_id}/edition`
- **Base URL:** `{dataCenterUrl}`
- **Official documentation:** [Switch Tenant Service Edition](https://developer.acronis.com/doc/outbound/apis/api-library/account/offering-items/switching-edition.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tenant_id` | path | `string` | yes | Tenant Id path parameter. |
