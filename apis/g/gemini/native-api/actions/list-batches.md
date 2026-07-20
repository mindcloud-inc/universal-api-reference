# List Batches with Gemini

Retrieves a list of batches from Gemini.

## Endpoint

- **Method:** `GET`
- **Path:** `v1beta/:name`
- **Base URL:** `https://generativelanguage.googleapis.com`
- **Official documentation:** [List Batches](https://ai.google.dev/api/batch-api#method:-batches.list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | query | `string` | no | Optional filter expression for batch listing. |
| `returnPartialSuccess` | query | `boolean` | no | Whether to return partial success results. |
