# Get Tenant with Permit.io

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/facts/:projId/:envId/tenants/:tenantId`
- **Base URL:** `https://api.permit.io`
- **Official documentation:** [Get Tenant](https://api.permit.io/scalar)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projId` | path | `string` | yes | Permit project identifier or key. |
| `envId` | path | `string` | yes | Permit environment identifier or key. |
| `tenantId` | path | `string` | yes | Permit tenant identifier. |
