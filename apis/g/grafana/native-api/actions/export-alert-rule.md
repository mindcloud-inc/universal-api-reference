# Export Alert Rule with Grafana

Exports an alert rule from Grafana.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/provisioning/alert-rules/:UID/export`
- **Base URL:** `https://apps78aa.grafana.net/api`
- **Official documentation:** [Export Alert Rule](https://grafana.com/docs/grafana/latest/alerting/set-up/provision-alerting-resources/http-api-provisioning/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `UID` | path | `string` | yes | The alert rule UID. |
