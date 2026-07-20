# Schedule Experiment Start with Statsig

Schedules an experiment start in Statsig.

## Endpoint

- **Method:** `POST`
- **Path:** `/console/v1/experiments/{id}/schedule_start`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Schedule Experiment Start](https://docs.statsig.com/api-reference/experiments/schedule-experiment-start)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | id |
| `scheduledTime` | body | `number` | yes | Request body field. |
