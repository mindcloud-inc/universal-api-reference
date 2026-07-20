# Create Folder with Zoho Sign

Creates a folder in Zoho Sign.

## Endpoint

- **Method:** `POST`
- **Path:** `/folders`
- **Base URL:** `https://sign.zoho.com/api/v1`
- **Official documentation:** [Create Folder](https://www.zoho.com/sign/api/document-managment/create-new-folder.html)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | yes | Zoho Sign folder payload wrapper. |
| `data.folders` | body | `object` | yes | Folder details. |
| `data.folders.folder_name` | body | `string` | yes | Name of the folder to create. |
