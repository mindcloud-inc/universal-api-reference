# Get Template with Grafana

Retrieves a template from Grafana.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/provisioning/templates/:name`
- **Base URL:** `https://apps78aa.grafana.net/api`
- **Official documentation:** [Get Template](https://grafana.com/docs/grafana/latest/alerting/set-up/provision-alerting-resources/http-api-provisioning/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | The template group name. |
