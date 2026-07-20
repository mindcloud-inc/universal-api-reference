# Get Translation Result with CAMB.AI

Retrieves a translation result from CAMB.AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/translation-result/:run_id`
- **Base URL:** `https://client.camb.ai/apis`
- **Official documentation:** [Get Translation Result](https://docs.camb.ai/api-reference/endpoint/get-translation-run-result)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `run_id` | path | `number` | yes | Run identifier returned by a completed translation task. |
