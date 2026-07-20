# Upload Knowledge Base File with Atlas AI Revenue Engine

## Endpoint

- **Method:** `POST`
- **Path:** `/knowledgebase/upload`
- **Base URL:** `https://api.youratlas.com/v1/api`
- **Official documentation:** [Upload Knowledge Base File](https://apidocs.youratlas.com/upload-knowledge-file-26917881e0)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/octet-stream` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | query | `string` | no | Optional campaign ID. |
| `filename` | query | `string` | yes | The filename. |
| `fileContent` | body | `file` | yes | Binary file content to upload. |
