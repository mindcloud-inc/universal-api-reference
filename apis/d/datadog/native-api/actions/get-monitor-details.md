# Get Monitor Details with Datadog

Retrieves monitor details from Datadog.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/monitor/:monitor_id`
- **Base URL:** `https://api.us5.datadoghq.com`
- **Official documentation:** [Get Monitor Details](https://docs.datadoghq.com/api/latest/monitors/#get-a-monitors-details)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group_states` | query | `string` | no | Comma-separated monitor group states to include: all, alert, warn, or no data. |
| `monitor_id` | path | `number` | yes | The ID of the monitor to retrieve. |
| `with_assets` | query | `boolean` | no | Include assets tied to the monitor in the returned response. |
| `with_downtimes` | query | `boolean` | no | Include current active downtimes for the monitor in the returned response. |
