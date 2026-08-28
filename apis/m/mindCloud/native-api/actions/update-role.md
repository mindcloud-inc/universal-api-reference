# Update Role with MindCloud

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/roles/:roleId`
- **Base URL:** `https://connect.mindcloud.co`
- **Official documentation:** [Update Role](https://connect.mindcloud.co/v2/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Description for this MindCloud v2 request. |
| `name` | body | `string` | no | Name for this MindCloud v2 request. |
| `permissions[]` | body | `array<string>` | no | Permissions for this MindCloud v2 request. |
| `roleId` | path | `string` | yes | Role ID for this MindCloud v2 request. |
