# Get Text-to-Speech Result with CAMB.AI

Retrieves a text-to-speech result from CAMB.AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/tts-result/:run_id`
- **Base URL:** `https://client.camb.ai/apis`
- **Official documentation:** [Get Text-to-Speech Result](https://docs.camb.ai/api-reference/endpoint/get-tts-run-info)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `run_id` | path | `number` | yes | Run identifier returned by a completed text-to-speech task. |
| `output_type` | query | `string` | no | Response mode for the result; use file_url for a downloadable URL. |
