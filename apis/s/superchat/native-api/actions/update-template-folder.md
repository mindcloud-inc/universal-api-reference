# Update Template Folder with Superchat

Updates an existing template folder in Superchat.

## Endpoint

- **Method:** `PUT`
- **Path:** `/template-folders/{folder_id}`
- **Base URL:** `https://api.superchat.com/v1.0`
- **Official documentation:** [Update Template Folder](https://developers.superchat.com/reference/updatetemplatefolder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folder_id` | path | `string` | yes | The `id` of the template folder |
| `name` | body | `string` | no | The name of the template folder |
