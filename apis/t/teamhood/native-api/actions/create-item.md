# Create Item with Teamhood

Creates a new item in Teamhood.

## Endpoint

- **Method:** `POST`
- **Path:** `/items`
- **Base URL:** `https://api-mindcloud1.teamhood.com/api/v1`
- **Official documentation:** [Create Item](https://api-mindcloud1.teamhood.com/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `boardId` | body | `string` | no | The board that will own the item. |
| `rowId` | body | `string` | no | The row that will contain the item. |
| `statusId` | body | `string` | no | The initial status for the item. |
| `title` | body | `string` | no | The item title. |
| `workspaceId` | body | `string` | no | The workspace that will own the item. |
