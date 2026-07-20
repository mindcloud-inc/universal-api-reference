# Get Generation Status with Alai

Retrieves async operation status from Alai.

## Endpoint

- **Method:** `GET`
- **Path:** `/generations/:generation_id`
- **Base URL:** `https://slides-api.getalai.com/api/v1`
- **Official documentation:** [Get Generation Status](https://docs.getalai.com/api/generation-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `generation_id` | path | `string` | yes | Generation identifier returned by an async create or export call. |
