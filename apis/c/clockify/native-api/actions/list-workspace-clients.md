# List Workspace Clients with Clockify

Lists all workspace clients in Clockify.

## Endpoint

- **Method:** `GET`
- **Path:** `workspaces/:workspaceId/clients`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [List Workspace Clients](https://docs.developer.clockify.me/#tag/Client/operation/getClients)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes | Workspace identifier. |
| `name` | query | `string` | no | Filter clients by name. |
| `archived` | query | `boolean` | no | Include archived clients. |
