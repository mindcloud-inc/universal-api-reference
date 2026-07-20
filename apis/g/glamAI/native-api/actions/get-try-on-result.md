# Get Try-On Result with Glam AI

Retrieves a try-on result from Glam AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/tryon/:event_id`
- **Base URL:** `https://api.glam.ai/api/v1`
- **Official documentation:** [Get Try-On Result](https://glam-ai.readme.io/reference/get_result_tryon__event_id__get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event_id` | path | `string` | yes | Try-on event ID returned by Create Try-On Generation. |
