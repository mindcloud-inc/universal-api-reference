# Conclude Experiment & Defer Decision with Statsig

Concludes an experiment and defers its decision in Statsig.

## Endpoint

- **Method:** `PUT`
- **Path:** `/console/v1/experiments/{id}/defer_decision`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Conclude Experiment & Defer Decision](https://docs.statsig.com/api-reference/experiments/conclude-experiment-defer-decision)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | id |
| `stopReason` | body | `string` | no | Request body field. |
