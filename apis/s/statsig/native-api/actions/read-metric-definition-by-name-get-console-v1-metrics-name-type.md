# Read Metric Definition by Name with Statsig

Retrieves a metric definition by name from Statsig.

## Endpoint

- **Method:** `GET`
- **Path:** `/console/v1/metrics/{name}/{type}`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Read Metric Definition by Name](https://docs.statsig.com/api-reference/metrics/read-metric-definition-by-name)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | name |
| `type` | path | `string` | yes | type |
