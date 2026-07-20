# List Lists with ClickUp

View the Lists within a Folder.

## Endpoint

- **Method:** `GET`
- **Path:** `folder/:folder_id/list`
- **Base URL:** `https://api.clickup.com/api/v2/`
- **Official documentation:** [List Lists](https://developer.clickup.com/reference/getlists)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folder_id` | path | `string` | yes | — |
| `archived` | query | `boolean` | no | Format: `toggle`. |
