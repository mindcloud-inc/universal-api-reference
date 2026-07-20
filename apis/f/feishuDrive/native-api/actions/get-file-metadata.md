# Get File Metadata with Feishu Drive

Retrieves file metadata from Feishu Drive.

## Endpoint

- **Method:** `POST`
- **Path:** `/drive/v1/metas/batch_query`
- **Base URL:** `https://open.feishu.cn/open-apis`
- **Official documentation:** [Get File Metadata](https://open.feishu.cn/document/uAjLw4CM/ukTMukTMukTM/reference/drive-v1/meta/batch_query)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `doc_token` | body | `string` | yes | Drive doc token for each requested document. |
| `doc_type` | body | `string` | yes | Drive doc type for each requested document, such as file or docx. |
| `request_docs[]` | body | `array<object>` | yes | Array of requested Drive docs. Each item must include doc_token and doc_type. |
| `with_url` | body | `boolean` | no | Whether to include the file URL in the metadata response. |
