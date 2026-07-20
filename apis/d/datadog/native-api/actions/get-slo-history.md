# Get SLO History with Datadog

Retrieves service level objective history from Datadog.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/slo/:slo_id/history`
- **Base URL:** `https://api.us5.datadoghq.com`
- **Official documentation:** [Get SLO History](https://docs.datadoghq.com/api/latest/service-level-objectives/#get-an-slos-history)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `slo_id` | path | `string` | yes | The ID of the service level objective. |
| `from_ts` | query | `number` | yes | Start of the history window in epoch seconds. |
| `to_ts` | query | `number` | yes | End of the history window in epoch seconds. |
| `target` | query | `number` | no | Optional custom SLO target. |
| `apply_correction` | query | `boolean` | no | Whether to apply SLO corrections. |
