# Update Folder with Stack AI

## Endpoint

- **Method:** `PATCH`
- **Path:** `/folders/:folder_id`
- **Base URL:** `https://api.stack-ai.com`
- **Official documentation:** [Update Folder](https://docs.stackai.com/api-reference/folders#patch-folders-folder_id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folder_id` | path | `string` | yes | The folder identifier. |
| `name` | body | `string` | no | The folder name. |
