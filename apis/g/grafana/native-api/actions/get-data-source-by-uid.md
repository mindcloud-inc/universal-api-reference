# Get Data Source By UID with Grafana

Retrieves a data source from Grafana by UID.

## Endpoint

- **Method:** `GET`
- **Path:** `/datasources/uid/:uid`
- **Base URL:** `https://apps78aa.grafana.net/api`
- **Official documentation:** [Get Data Source By UID](https://grafana.com/docs/grafana/latest/developer-resources/api-reference/http-api/data_source/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uid` | path | `string` | yes | The data source UID. |
