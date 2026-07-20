# List Documents with DocuPipe

Retrieves documents from DocuPipe.

## Endpoint

- **Method:** `GET`
- **Path:** `/documents`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [List Documents](https://docs.docupipe.ai/reference/list_documents)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dataset` | query | `string` | no | The dataset to filter documents by |
| `exclude_payload` | query | `boolean` | no | Whether to exclude the result payload from the response |
