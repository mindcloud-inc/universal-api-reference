# Search Standardizations with DocuPipe

Finds standardizations in DocuPipe.

## Endpoint

- **Method:** `GET`
- **Path:** `/standardizations/search`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Search Standardizations](https://docs.docupipe.ai/reference/search_standardizations)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Search query to match against filename, document ID, or standardization ID |
| `schema_id` | query | `string` | no | Optional schema ID filter |
| `dataset` | query | `string` | no | Optional dataset filter |
