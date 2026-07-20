# Get File Statistics with Feishu Drive

Retrieves file statistics from Feishu Drive.

## Endpoint

- **Method:** `GET`
- **Path:** `/drive/v1/files/:file_token/statistics`
- **Base URL:** `https://open.feishu.cn/open-apis`
- **Official documentation:** [Get File Statistics](https://open.feishu.cn/document/uAjLw4CM/ukTMukTMukTM/reference/drive-v1/file-statistics/get)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_token` | path | `string` | yes | Drive file token to inspect statistics for. |
| `file_type` | query | `string` | yes | Drive file type such as file, folder, or docx. |
