# Update Role with Statsig

Updates a role in Statsig.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/console/v1/roles/{id}`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Update Role](https://docs.statsig.com/api-reference/roles/update-role)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | id |
| `permissions` | body | `object` | yes | Request body field. |
