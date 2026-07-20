# Copy File with Feishu Drive

Creates a file copy in Feishu Drive.

## Endpoint

- **Method:** `POST`
- **Path:** `/drive/v1/files/:file_token/copy`
- **Base URL:** `https://open.feishu.cn/open-apis`
- **Official documentation:** [Copy File](https://open.feishu.cn/document/uAjLw4CM/ukTMukTMukTM/reference/drive-v1/file/copy)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_token` | path | `string` | yes | Source file token to copy. |
| `folder_token` | body | `string` | yes | Destination folder token for the copied file. |
| `name` | body | `string` | yes | Name for the copied file. |
| `type` | body | `string` | yes | Source file type, such as file or docx. |
