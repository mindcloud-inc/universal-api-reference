# Get Check Metrics with updown.io

Retrieves detailed check metrics from updown.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/checks/:token/metrics`
- **Base URL:** `https://updown.io/api`
- **Official documentation:** [Get Check Metrics](https://updown.io/api#GET-/api/checks/:token/metrics)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | query | `date` | no | Start time for the metrics window. |
| `group` | query | `list` | no | Group data by time or host. Accepted values: `host`, `time`. |
| `to` | query | `date` | no | End time for the metrics window. |
| `token` | path | `string` | yes | The check unique token. |
