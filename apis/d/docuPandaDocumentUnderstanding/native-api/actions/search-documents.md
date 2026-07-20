# Search Documents with DocuPanda - Document Understanding

Finds documents in DocuPanda by filename or document ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/documents/search`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Search Documents](https://docs.docupipe.ai/reference/search_documents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Search query to match against filename or document ID |
| `dataset` | query | `string` | no | Optional dataset filter |
| `limit` | query | `number` | no | Maximum number of results to return (1-500) |
| `offset` | query | `number` | no | Number of results to skip for pagination |
