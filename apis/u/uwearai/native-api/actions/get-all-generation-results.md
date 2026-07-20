# Get All Generation Results with Uwear.ai

Retrieves generation results from Uwear.ai.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/generation-results`
- **Base URL:** `https://api.uwear.ai`
- **Official documentation:** [Get All Generation Results](https://docs.dev.uwear.ai/operations/external_read_generation_results)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `clothing_item_id` | query | `number` | no | Optional clothing item ID filter. |
| `generation_id` | query | `number` | no | Optional generation request ID filter. |
