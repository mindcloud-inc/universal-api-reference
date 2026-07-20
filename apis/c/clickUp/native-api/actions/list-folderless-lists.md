# List Folderless Lists with ClickUp

View the Lists without a Folder

## Endpoint

- **Method:** `GET`
- **Path:** `space/:space_id/list`
- **Base URL:** `https://api.clickup.com/api/v2/`
- **Official documentation:** [List Folderless Lists](https://developer.clickup.com/reference/getfolderlesslists)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `space_id` | path | `string` | yes | — |
| `archived` | query | `boolean` | no | Format: `toggle`. |
