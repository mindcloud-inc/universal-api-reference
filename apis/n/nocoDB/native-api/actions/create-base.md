# Create Base with NocoDB

Creates a new base in NocoDB.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v3/meta/workspaces/:workspaceId/bases`
- **Base URL:** `https://app.nocodb.com`
- **Official documentation:** [Create Base](https://nocodb.com/apis/v3/meta)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes | Workspace identifier. |
| `title` | body | `string` | yes | Title of the base. |
