# Update Document with Smartcat

Updates an existing document in Smartcat.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/integration/v1/document/update`
- **Base URL:** `https://smartcat.ai`
- **Official documentation:** [Update Document](https://developers.smartcat.com/api/#update-the-specified-document)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | query | `string` | yes | Document ID in the format documentId_targetLanguageId |
| `REQUEST` | body | `object` | yes | JSON object with update options for the replacement document file. |
| `FILE` | body | `file` | yes | — |
