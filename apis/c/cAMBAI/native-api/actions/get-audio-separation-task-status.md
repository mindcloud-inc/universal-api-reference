# Get Audio Separation Task Status with CAMB.AI

Retrieves audio separation task status from CAMB.AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/audio-separation/:task_id`
- **Base URL:** `https://client.camb.ai/apis`
- **Official documentation:** [Get Audio Separation Task Status](https://docs.camb.ai/api-reference/endpoint/get-audio-separation-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | path | `string` | yes | Task identifier returned by Create Audio Separation. |
