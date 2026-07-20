# Create Workspace with Clockify

Creates a new workspace in Clockify.

## Endpoint

- **Method:** `POST`
- **Path:** `workspaces`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Create Workspace](https://docs.developer.clockify.me/#tag/Workspace/operation/createWorkspace)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Maximum length: 50. |
| `organizationId` | body | `string` | no | — |
