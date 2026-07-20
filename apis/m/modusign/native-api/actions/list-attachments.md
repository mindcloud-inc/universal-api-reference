# List Attachments with Modusign

Retrieves attachments for a document from Modusign.

## Endpoint

- **Method:** `GET`
- **Path:** `/documents/:documentId/attachments`
- **Base URL:** `https://api.modusign.co.kr`
- **Official documentation:** [List Attachments](https://developers.modusign.co.kr/reference/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `string` | yes | The Modusign document ID. |
