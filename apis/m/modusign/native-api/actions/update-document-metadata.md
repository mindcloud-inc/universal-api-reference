# Update Document Metadata with Modusign

Replaces existing document metadata in Modusign.

## Endpoint

- **Method:** `PUT`
- **Path:** `/documents/:documentId/metadatas`
- **Base URL:** `https://api.modusign.co.kr`
- **Official documentation:** [Update Document Metadata](https://developers.modusign.co.kr/reference/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `string` | yes | The Modusign document ID. |
| `metadatas[]` | body | `array<object>` | yes | The metadata entries to write on the document. |
