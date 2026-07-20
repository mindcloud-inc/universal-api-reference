# List Batches with Google AI Studio

Retrieves batch operations from Google AI Studio.

## Endpoint

- **Method:** `GET`
- **Path:** `v1beta/:name`
- **Base URL:** `https://generativelanguage.googleapis.com`
- **Official documentation:** [List Batches](https://ai.google.dev/api/batch-api)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | query | `string` | no | Optional filter expression for batch listing. |
| `returnPartialSuccess` | query | `boolean` | no | Whether to return partial success results. |
