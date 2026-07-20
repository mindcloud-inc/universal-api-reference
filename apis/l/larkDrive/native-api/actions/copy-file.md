# Copy File with Lark Drive

## Endpoint

- **Method:** `POST`
- **Path:** `/drive/v1/files/:file_token/copy`
- **Base URL:** `https://open.larksuite.com/open-apis`
- **Official documentation:** [Copy File](https://open.larksuite.com/document/uAjLw4CM/ukTMukTMukTM/reference/drive-v1/file/copy)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `file_token` | path | `string` | yes |
| `name` | body | `string` | yes |
| `type` | body | `string` | no |
| `folder_token` | body | `string` | yes |
