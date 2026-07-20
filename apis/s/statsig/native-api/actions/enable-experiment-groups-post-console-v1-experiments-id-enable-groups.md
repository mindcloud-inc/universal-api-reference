# Enable Experiment Groups with Statsig

Enables experiment groups in Statsig.

## Endpoint

- **Method:** `POST`
- **Path:** `/console/v1/experiments/{id}/enable_groups`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Enable Experiment Groups](https://docs.statsig.com/api-reference/experiments/enable-experiment-groups)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | id |
| `group_names` | body | `list` | yes | Request body field. |
