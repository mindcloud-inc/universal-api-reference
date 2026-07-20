# Create Folder with Trint

Creates a new folder in Trint.

## Endpoint

- **Method:** `POST`
- **Path:** `/folders/`
- **Base URL:** `https://api.trint.com`
- **Official documentation:** [Create Folder](https://dev.trint.com/reference/page-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Folder name. |
| `parentId` | body | `string` | no | Parent folder identifier for nested folders. |
| `workspaceId` | body | `string` | no | Shared drive identifier when creating a folder inside a shared drive. |
