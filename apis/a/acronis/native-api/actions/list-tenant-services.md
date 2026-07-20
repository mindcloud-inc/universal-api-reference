# List Tenant Services with Acronis

Retrieves services enabled for a tenant in Acronis.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/2/tenants/{tenant_id}/applications`
- **Base URL:** `{dataCenterUrl}`
- **Official documentation:** [List Tenant Services](https://developer.acronis.com/doc/outbound/apis/api-library/account/services/fetching-services.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tenant_id` | path | `string` | yes | Tenant Id path parameter. |
