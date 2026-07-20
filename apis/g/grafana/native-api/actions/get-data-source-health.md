# Get Data Source Health with Grafana

Retrieves data source health from Grafana.

## Endpoint

- **Method:** `GET`
- **Path:** `/datasources/uid/:uid/health`
- **Base URL:** `https://apps78aa.grafana.net/api`
- **Official documentation:** [Get Data Source Health](https://grafana.com/docs/grafana/latest/developer-resources/api-reference/http-api/data_source/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uid` | path | `string` | yes | The data source UID. |
