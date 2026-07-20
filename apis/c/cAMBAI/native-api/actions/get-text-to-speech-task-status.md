# Get Text-to-Speech Task Status with CAMB.AI

Retrieves text-to-speech task status from CAMB.AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/tts/:task_id`
- **Base URL:** `https://client.camb.ai/apis`
- **Official documentation:** [Get Text-to-Speech Task Status](https://docs.camb.ai/api-reference/endpoint/get-tts-result)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | path | `string` | yes | Task identifier returned by Create Text-to-Speech. |
