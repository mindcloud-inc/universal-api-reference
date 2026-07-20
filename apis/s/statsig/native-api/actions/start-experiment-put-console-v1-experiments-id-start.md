# Start Experiment with Statsig

Starts an experiment in Statsig.

## Endpoint

- **Method:** `PUT`
- **Path:** `/console/v1/experiments/{id}/start`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Start Experiment](https://docs.statsig.com/api-reference/experiments/start-experiment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | id |
| `analysisStartTime` | body | `string` | no | Request body field. |
| `analysisEndTime` | body | `string` | no | Request body field. |
| `turboMode` | body | `boolean` | no | Request body field. |
