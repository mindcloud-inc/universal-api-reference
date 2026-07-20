# Replace Folder with Porsline

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/folders/:folder_id/`
- **Base URL:** `https://survey.porsline.com`
- **Official documentation:** [Replace Folder](https://developers.porsline.com/#tag/Folders/paths/~1api~1folders~1{folder_id}~1/put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folder_id` | path | `number` | yes | Selected folder id. |
| `name` | body | `string` | yes | The name of the folder. |
| `order` | body | `number` | no | The folder order. |
