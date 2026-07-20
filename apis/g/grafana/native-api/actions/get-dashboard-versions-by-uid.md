# Get Dashboard Versions By UID with Grafana

Retrieves dashboard versions from Grafana by UID.

## Endpoint

- **Method:** `GET`
- **Path:** `/dashboards/uid/:uid/versions`
- **Base URL:** `https://apps78aa.grafana.net/api`
- **Official documentation:** [Get Dashboard Versions By UID](https://grafana.com/docs/grafana/latest/developer-resources/api-reference/http-api/dashboard_versions/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uid` | path | `string` | yes | The dashboard UID. |
