# Archive Experiment with Statsig

Archives an experiment in Statsig.

## Endpoint

- **Method:** `PUT`
- **Path:** `/console/v1/experiments/{id}/archive`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Archive Experiment](https://docs.statsig.com/api-reference/experiments/archive-experiment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | id |
| `archiveReason` | body | `string` | no | Request body field. |
