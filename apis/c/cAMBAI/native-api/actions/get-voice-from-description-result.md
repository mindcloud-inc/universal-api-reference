# Get Voice from Description Result with CAMB.AI

Retrieves a voice-from-description result from CAMB.AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/text-to-voice-result/:run_id`
- **Base URL:** `https://client.camb.ai/apis`
- **Official documentation:** [Get Voice from Description Result](https://docs.camb.ai/api-reference/endpoint/get-text-to-voice-run-result)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `run_id` | path | `number` | yes | Run identifier returned by a completed voice generation task. |
