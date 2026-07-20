# Get Generation Result with Glam AI

Retrieves an image generation result from Glam AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/result/:event_id`
- **Base URL:** `https://api.glam.ai/api/v1`
- **Official documentation:** [Get Generation Result](https://glam-ai.readme.io/reference/get_result_result__event_id__get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event_id` | path | `string` | yes | Generation event ID returned by Create Generation. |
