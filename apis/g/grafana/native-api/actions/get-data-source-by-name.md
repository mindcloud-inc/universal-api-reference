# Get Data Source By Name with Grafana

Retrieves a data source from Grafana by name.

## Endpoint

- **Method:** `GET`
- **Path:** `/datasources/name/:name`
- **Base URL:** `https://apps78aa.grafana.net/api`
- **Official documentation:** [Get Data Source By Name](https://grafana.com/docs/grafana/latest/developer-resources/api-reference/http-api/data_source/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | The data source name. |
