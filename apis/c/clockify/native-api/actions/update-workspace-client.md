# Update Workspace Client with Clockify

Updates an existing workspace client in Clockify.

## Endpoint

- **Method:** `PUT`
- **Path:** `workspaces/:workspaceId/clients/:id`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Update Workspace Client](https://docs.developer.clockify.me/#tag/Client/operation/updateClient)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes | Workspace identifier. |
| `id` | path | `string` | yes | Client identifier. |
| `name` | body | `string` | no | Client name. |
| `email` | body | `string` | no | Client email. |
| `address` | body | `string` | no | Client address. |
| `note` | body | `string` | no | Client note. |
| `archived` | body | `boolean` | no | Archive state. |
| `ccEmails[]` | body | `array<string>` | no | Additional invoice emails. |
| `currencyId` | body | `string` | no | Currency identifier. |
| `archive-projects` | query | `boolean` | no | Archive related projects. |
| `mark-tasks-as-done` | query | `boolean` | no | Mark tasks as done when archiving. |
