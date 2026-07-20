# Get Dashboard Version By UID with Grafana

Retrieves a dashboard version from Grafana by UID.

## Endpoint

- **Method:** `GET`
- **Path:** `/dashboards/uid/:uid/versions/:DashboardVersionID`
- **Base URL:** `https://apps78aa.grafana.net/api`
- **Official documentation:** [Get Dashboard Version By UID](https://grafana.com/docs/grafana/latest/developer-resources/api-reference/http-api/dashboard_versions/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uid` | path | `string` | yes | The dashboard UID. |
| `DashboardVersionID` | path | `number` | yes | The dashboard version ID. |
