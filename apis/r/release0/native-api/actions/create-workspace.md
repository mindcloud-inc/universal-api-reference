# Create Workspace with Release0

Creates a new workspace in Release0.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/workspaces`
- **Base URL:** `https://release0.com/api`
- **Official documentation:** [Create Workspace](https://docs.release0.com/api-reference/workspace/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The workspace name. |
| `slug` | body | `string` | no | The workspace slug. |
