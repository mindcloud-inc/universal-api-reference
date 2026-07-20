# Remove Document Label with Modusign

Removes a label from a document in Modusign.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/documents/:documentId/labels/:labelId`
- **Base URL:** `https://api.modusign.co.kr`
- **Official documentation:** [Remove Document Label](https://developers.modusign.co.kr/reference/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `string` | yes | The Modusign document ID. |
| `labelId` | path | `string` | yes | The Modusign label ID. |
