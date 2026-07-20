# Move File or Folder with Feishu Drive

Moves a file or folder in Feishu Drive.

## Endpoint

- **Method:** `POST`
- **Path:** `/drive/v1/files/:file_token/move`
- **Base URL:** `https://open.feishu.cn/open-apis`
- **Official documentation:** [Move File or Folder](https://open.feishu.cn/document/uAjLw4CM/ukTMukTMukTM/reference/drive-v1/file/move)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_token` | path | `string` | yes | File or folder token to move. |
| `folder_token` | body | `string` | yes | Destination folder token. |
| `type` | body | `string` | yes | File or folder type to move. |
