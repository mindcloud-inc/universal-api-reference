# List Standardizations with DocuPipe

Retrieves standardizations from DocuPipe.

## Endpoint

- **Method:** `GET`
- **Path:** `/standardizations`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [List Standardizations](https://docs.docupipe.ai/reference/list_standardizations)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `schema_id` | query | `string` | no | The schema ID to filter standardizations by |
| `document_id` | query | `string` | no | The ID of the document to filter standardizations by |
| `exclude_payload` | query | `boolean` | no | Whether to exclude the data payload in the response |
