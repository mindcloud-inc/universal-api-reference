# Create Folder with Lark Drive

## Endpoint

- **Method:** `POST`
- **Path:** `/drive/v1/files/create_folder`
- **Base URL:** `https://open.larksuite.com/open-apis`
- **Official documentation:** [Create Folder](https://open.larksuite.com/document/uAjLw4CM/ukTMukTMukTM/reference/drive-v1/file/create_folder)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `folder_token` | body | `string` | yes |
