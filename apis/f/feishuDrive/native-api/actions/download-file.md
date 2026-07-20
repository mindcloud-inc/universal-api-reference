# Download File with Feishu Drive

Retrieves a file download from Feishu Drive.

## Endpoint

- **Method:** `GET`
- **Path:** `/drive/v1/files/:file_token/download`
- **Base URL:** `https://open.feishu.cn/open-apis`
- **Official documentation:** [Download File](https://open.feishu.cn/document/uAjLw4CM/ukTMukTMukTM/reference/drive-v1/file/download)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_token` | path | `string` | yes | The Feishu Drive file_token for the file to download. |
