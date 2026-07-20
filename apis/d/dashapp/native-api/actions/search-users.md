# Search Users with Dash.app

Finds users in Dash.app by search criteria.

## Endpoint

- **Method:** `POST`
- **Path:** `/user-searches`
- **Base URL:** `https://api-v2.dash.app`
- **Official documentation:** [Search Users](https://api-docs.dash.app/dash/openapi/users/postusersearch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | body | `number` | yes | The item number to begin the result set from. |
| `pageSize` | body | `number` | yes | The maximum number of items to return. |
| `criterion` | body | `object` | yes | Dash user search criterion object. |
| `sorts[]` | body | `array<object>` | no | Dash user sort array. |
