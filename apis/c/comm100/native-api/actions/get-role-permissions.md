# Get Role Permissions with Comm100

Retrieves permissions for a role from Comm100 settings.

## Endpoint

- **Method:** `GET`
- **Path:** `global/roles/{{id}}/permissions`
- **Base URL:** `https://api17.comm100.io/v4`
- **Official documentation:** [Get Role Permissions](https://developer.comm100.com/docs/server-api-global-setting-permission)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Comm100 role ID. |
