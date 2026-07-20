# List Standardizations with DocuPanda - Document Understanding

Retrieves standardizations from DocuPanda.

## Endpoint

- **Method:** `GET`
- **Path:** `/standardizations`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [List Standardizations](https://docs.docupipe.ai/reference/list_standardizations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `schema_id` | query | `string` | no | The schema ID to filter standardizations by |
| `document_id` | query | `string` | no | The ID of the document to filter standardizations by |
| `limit` | query | `number` | no | The maximum number of standardizations to return. Maximum is 1000 |
| `offset` | query | `number` | no | The number of standardizations to skip (to paginate through the data) |
| `exclude_payload` | query | `boolean` | no | Whether to exclude the data payload in the response |
