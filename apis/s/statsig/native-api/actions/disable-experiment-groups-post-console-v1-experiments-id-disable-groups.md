# Disable Experiment Groups with Statsig

Disables experiment groups in Statsig.

## Endpoint

- **Method:** `POST`
- **Path:** `/console/v1/experiments/{id}/disable_groups`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Disable Experiment Groups](https://docs.statsig.com/api-reference/experiments/disable-experiment-groups)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | id |
| `group_names` | body | `list` | yes | Request body field. |
