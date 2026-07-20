# Get All Generations with Uwear.ai

Retrieves generations from Uwear.ai.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/generations`
- **Base URL:** `https://api.uwear.ai`
- **Official documentation:** [Get All Generations](https://docs.dev.uwear.ai/operations/external_read_generations)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `clothing_item_id` | query | `number` | no | Optional clothing item ID filter. |
| `include` | query | `string` | no | Optional include expansion string supported by Uwear. |
| `status` | query | `string` | no | Optional generation status filter. |
