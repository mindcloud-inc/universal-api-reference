# List Files with Feishu Drive

Retrieves files from Feishu Drive.

## Endpoint

- **Method:** `GET`
- **Path:** `/drive/v1/files`
- **Base URL:** `https://open.feishu.cn/open-apis`
- **Official documentation:** [List Files](https://open.feishu.cn/document/uAjLw4CM/ukTMukTMukTM/reference/drive-v1/file/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folder_token` | query | `string` | no | Optional folder token. Leave empty to list the root Drive folder. |
| `page_size` | query | `number` | no | Optional page size for paginated folder listings. |
| `page_token` | query | `string` | no | Optional page token returned by a previous list call. |
