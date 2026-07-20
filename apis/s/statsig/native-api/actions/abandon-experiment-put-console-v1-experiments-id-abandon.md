# Abandon Experiment with Statsig

Abandons an experiment in Statsig.

## Endpoint

- **Method:** `PUT`
- **Path:** `/console/v1/experiments/{id}/abandon`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Abandon Experiment](https://docs.statsig.com/api-reference/experiments/abandon-experiment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | id |
| `decisionReason` | body | `string` | yes | Request body field. |
