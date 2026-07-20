# Update Experiment Overrides with Statsig

Updates experiment overrides in Statsig.

## Endpoint

- **Method:** `POST`
- **Path:** `/console/v1/experiments/{id}/overrides`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Update Experiment Overrides](https://docs.statsig.com/api-reference/experiments/update-experiment-overrides)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | id |
| `overrides` | body | `list` | yes | Request body field. |
| `userIDOverrides` | body | `list` | yes | Request body field. |
