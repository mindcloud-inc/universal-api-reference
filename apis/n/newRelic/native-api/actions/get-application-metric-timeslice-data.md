# Get Application Metric Timeslice Data with New Relic

Retrieves application metric timeslice data from New Relic.

## Endpoint

- **Method:** `GET`
- **Path:** `/applications/:appId/metrics/data.json`
- **Base URL:** `https://api.newrelic.com/v2`
- **Official documentation:** [Get Application Metric Timeslice Data](https://docs.newrelic.com/docs/apis/rest-api-v2/application-examples-v2/list-your-app-id-metric-timeslice-data-v2/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `number` | yes | New Relic application ID. |
