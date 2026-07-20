# Get Resolution Time Metrics with Rollbar

Retrieves resolution time metrics from Rollbar.

## Endpoint

- **Method:** `POST`
- **Path:** `/metrics/ttr`
- **Base URL:** `https://api.rollbar.com/api/1`
- **Official documentation:** [Get Resolution Time Metrics](https://docs.rollbar.com/reference/post_api-1-metrics-ttr)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_ids` | body | `string` | yes | List of Rollbar project IDs |
| `start_time` | body | `number` | yes | Unix timestamp of the query start time |
