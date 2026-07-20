# Get Translated Text-to-Speech Status with CAMB.AI

Retrieves translated text-to-speech task status from CAMB.AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/translated-tts/:task_id`
- **Base URL:** `https://client.camb.ai/apis`
- **Official documentation:** [Get Translated Text-to-Speech Status](https://docs.camb.ai/api-reference/endpoint/poll-translated-tts-result)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | path | `string` | yes | Task identifier returned by Create Translated Text-to-Speech. |
