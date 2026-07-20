# Update Folder with Porsline

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/folders/:folder_id/`
- **Base URL:** `https://survey.porsline.com`
- **Official documentation:** [Update Folder](https://developers.porsline.com/#tag/Folders/paths/~1api~1folders~1{folder_id}~1/patch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folder_id` | path | `number` | yes | Selected folder id. |
| `name` | body | `string` | no | The name of the folder. |
| `order` | body | `number` | no | The folder order. |
