# Create File Shortcut with Feishu Drive

Creates a file shortcut in Feishu Drive.

## Endpoint

- **Method:** `POST`
- **Path:** `/drive/v1/files/create_shortcut`
- **Base URL:** `https://open.feishu.cn/open-apis`
- **Official documentation:** [Create File Shortcut](https://open.feishu.cn/document/uAjLw4CM/ukTMukTMukTM/reference/drive-v1/file/create_shortcut)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `parent_token` | body | `string` | yes | Destination parent folder token for the shortcut. |
| `referToken` | body | `string` | yes | Source file token for the shortcut target. |
| `referType` | body | `string` | yes | Source file type for the shortcut target. |
