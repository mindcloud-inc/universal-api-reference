# Restart As New Experiment with Statsig

Restarts an experiment as new in Statsig.

## Endpoint

- **Method:** `POST`
- **Path:** `/console/v1/experiments/{id}/restart_as_new`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Restart As New Experiment](https://docs.statsig.com/api-reference/experiments/restart-as-new-experiment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | id |
| `name` | body | `string` | yes | Request body field. |
