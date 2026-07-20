# Get Dashboard By UID with Grafana

Retrieves a dashboard from Grafana by UID.

## Endpoint

- **Method:** `GET`
- **Path:** `/dashboards/uid/:uid`
- **Base URL:** `https://apps78aa.grafana.net/api`
- **Official documentation:** [Get Dashboard By UID](https://grafana.com/docs/grafana/latest/developer-resources/api-reference/http-api/dashboard/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uid` | path | `string` | yes | The dashboard UID. |
