# Retrieve branch metrics with Xata

## Endpoint

- **Method:** `POST`
- **Path:** `/organizations/:organizationID/projects/:projectID/branches/:branchID/metrics`
- **Base URL:** `https://api.xata.tech`
- **Official documentation:** [Retrieve branch metrics](https://xata.io/docs/api-reference/branches/retrieve-branch-metrics)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationID` | path | `string` | yes | — |
| `projectID` | path | `string` | yes | — |
| `branchID` | path | `string` | yes | — |
| `start` | body | `date` | yes | Start time |
| `end` | body | `date` | yes | End time |
| `metric` | body | `string` | yes | Metric name to query |
| `instances[]` | body | `array` | yes | List of instance IDs to query |
| `aggregations[]` | body | `array` | yes | List of aggregations to get, this is how the data-points within the interval are aggregated. Each one will generate a separate time-series in the response. |
