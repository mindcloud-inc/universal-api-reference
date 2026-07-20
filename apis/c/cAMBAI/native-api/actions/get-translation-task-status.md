# Get Translation Task Status with CAMB.AI

Retrieves translation task status from CAMB.AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/translate/:task_id`
- **Base URL:** `https://client.camb.ai/apis`
- **Official documentation:** [Get Translation Task Status](https://docs.camb.ai/api-reference/endpoint/poll-translation-result)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | path | `string` | yes | Task identifier returned by Create Translation. |
