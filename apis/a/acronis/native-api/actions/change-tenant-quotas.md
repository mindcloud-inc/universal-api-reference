# Change Tenant Quotas with Acronis

Updates tenant offering item quotas in Acronis.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/2/tenants/{tenant_id}/offering_items`
- **Base URL:** `{dataCenterUrl}`
- **Official documentation:** [Change Tenant Quotas](https://developer.acronis.com/doc/outbound/apis/api-library/account/offering-items/changing-quotas.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tenant_id` | path | `string` | yes | Tenant Id path parameter. |
