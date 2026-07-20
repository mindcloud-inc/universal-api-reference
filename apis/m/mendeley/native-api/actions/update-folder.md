# Update Folder with Mendeley

## Endpoint

- **Method:** `PATCH`
- **Path:** `/folders/:id`
- **Base URL:** `https://api.mendeley.com`
- **Official documentation:** [Update Folder](https://dev.mendeley.com/methods/#updating-a-folder)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/vnd.mendeley-folder.1+json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Identifier of the folder. |
| `name` | body | `string` | yes | Updated folder name. |
