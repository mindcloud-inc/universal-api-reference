# Create Tenant with Permit.io

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/facts/:projId/:envId/tenants`
- **Base URL:** `https://api.permit.io`
- **Official documentation:** [Create Tenant](https://api.permit.io/scalar)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projId` | path | `string` | yes | Permit project identifier or key. |
| `envId` | path | `string` | yes | Permit environment identifier or key. |
| `key` | body | `string` | yes | Unique tenant key within the Permit environment. |
| `name` | body | `string` | yes | Tenant display name. |
| `description` | body | `string` | no | Tenant description. |
| `attributes` | body | `object` | no | Custom tenant attributes object. |
