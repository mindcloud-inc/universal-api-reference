# Search Documents with DocuPipe

Finds documents in DocuPipe.

## Endpoint

- **Method:** `GET`
- **Path:** `/documents/search`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Search Documents](https://docs.docupipe.ai/reference/search_documents)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Search query to match against filename or document ID |
| `dataset` | query | `string` | no | Optional dataset filter |
