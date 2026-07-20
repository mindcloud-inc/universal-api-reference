# Get Sound and Music Result with CAMB.AI

Retrieves a sound or music result from CAMB.AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/text-to-sound-result/:run_id`
- **Base URL:** `https://client.camb.ai/apis`
- **Official documentation:** [Get Sound and Music Result](https://docs.camb.ai/api-reference/endpoint/get-text-to-sound-run-result)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `run_id` | path | `number` | yes | Run identifier returned by a completed sound or music task. |
| `output_type` | query | `string` | no | Response mode for the result; use file_url for a downloadable URL. |
