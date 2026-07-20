# Search Standardizations with DocuPanda - Document Understanding

Finds standardizations in DocuPanda by filename or IDs.

## Endpoint

- **Method:** `GET`
- **Path:** `/standardizations/search`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Search Standardizations](https://docs.docupipe.ai/reference/search_standardizations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dataset` | query | `string` | no | Optional dataset filter |
| `limit` | query | `number` | no | Maximum number of results to return (1-500) |
| `offset` | query | `number` | no | Number of results to skip for pagination |
| `query` | query | `string` | yes | Search query to match against filename, document ID, or standardization ID |
| `schema_id` | query | `string` | no | Optional schema ID filter |
