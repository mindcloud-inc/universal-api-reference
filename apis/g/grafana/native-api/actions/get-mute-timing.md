# Get Mute Timing with Grafana

Retrieves a mute timing from Grafana.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/provisioning/mute-timings/:name`
- **Base URL:** `https://apps78aa.grafana.net/api`
- **Official documentation:** [Get Mute Timing](https://grafana.com/docs/grafana/latest/alerting/set-up/provision-alerting-resources/http-api-provisioning/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | The mute timing name. |
