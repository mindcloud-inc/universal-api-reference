# Get Audio Separation Result with CAMB.AI

Retrieves an audio separation result from CAMB.AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/audio-separation-result/:run_id`
- **Base URL:** `https://client.camb.ai/apis`
- **Official documentation:** [Get Audio Separation Result](https://docs.camb.ai/api-reference/endpoint/get-audio-separation-run-info)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `run_id` | path | `number` | yes | Run identifier returned by a completed audio separation task. |
