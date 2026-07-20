# Get Alert Rule with Grafana

Retrieves an alert rule from Grafana.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/provisioning/alert-rules/:UID`
- **Base URL:** `https://apps78aa.grafana.net/api`
- **Official documentation:** [Get Alert Rule](https://grafana.com/docs/grafana/latest/alerting/set-up/provision-alerting-resources/http-api-provisioning/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `UID` | path | `string` | yes | The alert rule UID. |
