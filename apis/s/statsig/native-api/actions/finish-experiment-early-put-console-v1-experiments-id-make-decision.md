# Finish Experiment Early with Statsig

Finishes an experiment early in Statsig.

## Endpoint

- **Method:** `PUT`
- **Path:** `/console/v1/experiments/{id}/make_decision`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Finish Experiment Early](https://docs.statsig.com/api-reference/experiments/finish-experiment-early)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | id |
| `decisionReason` | body | `string` | yes | Request body field. |
| `removeTargeting` | body | `boolean` | no | Request body field. |
