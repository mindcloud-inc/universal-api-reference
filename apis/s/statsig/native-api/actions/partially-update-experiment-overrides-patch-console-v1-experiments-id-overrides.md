# Partially Update Experiment Overrides with Statsig

Updates experiment overrides in Statsig.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/console/v1/experiments/{id}/overrides`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Partially Update Experiment Overrides](https://docs.statsig.com/api-reference/experiments/partially-update-experiment-overrides)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | id |
| `overrides` | body | `list` | yes | Request body field. |
| `userIDOverrides` | body | `list` | yes | Request body field. |
