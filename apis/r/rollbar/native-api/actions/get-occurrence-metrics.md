# Get Occurrence Metrics with Rollbar

Retrieves occurrence metrics from Rollbar.

## Endpoint

- **Method:** `POST`
- **Path:** `/metrics/occurrences`
- **Base URL:** `https://api.rollbar.com/api/1`
- **Official documentation:** [Get Occurrence Metrics](https://docs.rollbar.com/reference/post_api-1-metrics-occurrences)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `end_time` | body | `number` | yes | Unix timestamp of the query end time |
| `start_time` | body | `number` | yes | Unix timestamp of the query start time |
