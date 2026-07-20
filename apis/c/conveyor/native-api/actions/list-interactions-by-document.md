# List Interactions By Document with Conveyor

Retrieves interactions for a document from Conveyor.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/interactions/documents/:document_id`
- **Base URL:** `https://api.conveyor.com/api`
- **Official documentation:** [List Interactions By Document](https://docs.conveyor.com/reference/get-interactions-by-document-id)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_id` | path | `string` | yes | Document identifier. |
| `created_at_start` | query | `date` | no | Start of created-at date range. |
| `created_at_end` | query | `date` | no | End of created-at date range. |
