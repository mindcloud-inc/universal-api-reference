# Get Client with Clockify

Retrieves a specific client from Clockify.

## Endpoint

- **Method:** `GET`
- **Path:** `workspaces/:workspaceId/clients/:id`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Get Client](https://docs.developer.clockify.me/#tag/Client/operation/getClient)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `id` | path | `string<string>` | yes |
