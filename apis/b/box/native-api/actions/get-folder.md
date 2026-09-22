# Get Folder with Box

## Endpoint

- **Method:** `GET`
- **Path:** `/folders/:folder_id`
- **Base URL:** `https://api.box.com/2.0`
- **Official documentation:** [Get Folder](https://developer.box.com/reference/get-folders-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields` | query | `string` | no | Optional comma-separated list of folder fields to include in the response. |
| `folder_id` | path | `string` | yes | The Box folder ID. Use `0` for the root folder. |
