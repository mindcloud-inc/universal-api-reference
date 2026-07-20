# Create Workspace Client with Clockify

Creates a new workspace client in Clockify.

## Endpoint

- **Method:** `POST`
- **Path:** `workspaces/:workspaceId/clients`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Create Workspace Client](https://docs.developer.clockify.me/#tag/Client/operation/createClient)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes | Workspace identifier. |
| `name` | body | `string` | yes | Client name. |
| `email` | body | `string` | no | Client email. |
| `address` | body | `string` | no | Client address. |
| `note` | body | `string` | no | Client note. |
