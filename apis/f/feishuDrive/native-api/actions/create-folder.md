# Create Folder with Feishu Drive

Creates a new folder in Feishu Drive.

## Endpoint

- **Method:** `POST`
- **Path:** `/drive/v1/files/create_folder`
- **Base URL:** `https://open.feishu.cn/open-apis`
- **Official documentation:** [Create Folder](https://open.feishu.cn/document/uAjLw4CM/ukTMukTMukTM/reference/drive-v1/file/create_folder)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folder_token` | body | `string` | yes | Parent folder token. Use an empty string for the root folder. |
| `name` | body | `string` | yes | Folder name to create. |
