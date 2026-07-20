# Add Folder with NewsBlur

Creates a folder in NewsBlur.

## Endpoint

- **Method:** `POST`
- **Path:** `/reader/add_folder`
- **Base URL:** `https://www.newsblur.com`
- **Official documentation:** [Add Folder](https://newsblur.com/api)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folder` | body | `string` | yes | Folder name to create. |
| `parent_folder` | body | `string` | no | Existing parent folder. Omit for top level. |
