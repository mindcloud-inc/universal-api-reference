# Upload Files to Classification with Extracta.ai

Uploads files to a classification in Extracta.ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/documentClassification/uploadFiles`
- **Base URL:** `https://api.extracta.ai/api/v1`
- **Official documentation:** [Upload Files to Classification](https://docs.extracta.ai/document-classification-api/api-endpoints-document-classification/5.-upload-files)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `classificationId` | body | `string` | yes | Unique identifier for the classification. |
| `files` | body | `file` | yes | One or more files to upload. Send multiple values as a array. |
