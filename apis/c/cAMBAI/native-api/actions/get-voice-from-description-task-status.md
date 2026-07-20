# Get Voice from Description Task Status with CAMB.AI

Retrieves voice-from-description task status from CAMB.AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/text-to-voice/:task_id`
- **Base URL:** `https://client.camb.ai/apis`
- **Official documentation:** [Get Voice from Description Task Status](https://docs.camb.ai/api-reference/endpoint/get-text-to-voice-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | path | `string` | yes | Task identifier returned by Create Voice from Description. |
