# Add Document Label with Modusign

Adds a label to a document in Modusign.

## Endpoint

- **Method:** `POST`
- **Path:** `/documents/:documentId/labels`
- **Base URL:** `https://api.modusign.co.kr`
- **Official documentation:** [Add Document Label](https://developers.modusign.co.kr/reference/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `string` | yes | The Modusign document ID. |
| `labelIds[]` | body | `array<string>` | yes | One to five Modusign label IDs to attach to the document. |
