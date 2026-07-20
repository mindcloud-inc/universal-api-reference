# Create Role with Statsig

Creates a role in Statsig.

## Endpoint

- **Method:** `POST`
- **Path:** `/console/v1/roles`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Create Role](https://docs.statsig.com/api-reference/roles/create-role)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Request body field. |
| `permissions` | body | `object` | yes | Request body field. |
