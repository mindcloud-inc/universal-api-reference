# Update Folder with Templated

Updates an existing folder in Templated.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/folder/:id`
- **Base URL:** `https://api.templated.io`
- **Official documentation:** [Update Folder](https://templated.io/docs/folders/update/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique identifier of the folder you want to update. |
| `name` | body | `string` | yes | The new name for the folder. |
