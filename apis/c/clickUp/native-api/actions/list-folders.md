# List Folders with ClickUp

View the Folders in a Space.

## Endpoint

- **Method:** `GET`
- **Path:** `space/:space_id/folder`
- **Base URL:** `https://api.clickup.com/api/v2/`
- **Official documentation:** [List Folders](https://developer.clickup.com/reference/getfolders)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `space_id` | path | `string` | yes | — |
| `archived` | query | `boolean` | no | Format: `toggle`. |
