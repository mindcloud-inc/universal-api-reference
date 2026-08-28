# Create Role with MindCloud

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/roles`
- **Base URL:** `https://connect.mindcloud.co`
- **Official documentation:** [Create Role](https://connect.mindcloud.co/v2/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Description for this MindCloud v2 request. |
| `name` | body | `string` | yes | Name for this MindCloud v2 request. |
| `permissions[]` | body | `array<string>` | no | Permissions for this MindCloud v2 request. |
