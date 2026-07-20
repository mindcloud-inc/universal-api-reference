# Delete File or Folder with Feishu Drive

Deletes a file or folder from Feishu Drive.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/drive/v1/files/:file_token`
- **Base URL:** `https://open.feishu.cn/open-apis`
- **Official documentation:** [Delete File or Folder](https://open.feishu.cn/document/uAjLw4CM/ukTMukTMukTM/reference/drive-v1/file/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_token` | path | `string` | yes | File or folder token to delete. |
| `type` | query | `string` | yes | File or folder type to delete. |
