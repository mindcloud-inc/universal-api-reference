# Delete Client with Clockify

Deletes an existing client from Clockify.

## Endpoint

- **Method:** `DELETE`
- **Path:** `workspaces/:workspaceId/clients/:id`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Delete Client](https://docs.developer.clockify.me/#tag/Client/operation/deleteClient)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `id` | path | `string<string>` | yes |
