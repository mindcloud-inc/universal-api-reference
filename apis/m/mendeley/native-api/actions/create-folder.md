# Create Folder with Mendeley

## Endpoint

- **Method:** `POST`
- **Path:** `/folders`
- **Base URL:** `https://api.mendeley.com`
- **Official documentation:** [Create Folder](https://dev.mendeley.com/methods/#creating-a-folder)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/vnd.mendeley-folder.1+json` |
| `Content-Type` | `application/vnd.mendeley-folder.1+json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name of the folder to create. |
