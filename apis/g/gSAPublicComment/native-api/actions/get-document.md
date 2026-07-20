# Get Document with GSA Public Comment

Retrieves a specific document from GSA Public Comment.

## Endpoint

- **Method:** `GET`
- **Path:** `/documents/:documentId`
- **Base URL:** `https://api.regulations.gov/v4`
- **Official documentation:** [Get Document](https://open.gsa.gov/api/regulationsgov/#detailed-information-for-a-single-document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `string` | yes | ID of the document to return. |
| `include` | query | `string` | no | Use attachments to include attachments in the response. |
