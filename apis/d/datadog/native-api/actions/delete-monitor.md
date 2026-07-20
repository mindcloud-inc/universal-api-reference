# Delete Monitor with Datadog

Deletes an existing monitor from Datadog.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v1/monitor/:monitor_id`
- **Base URL:** `https://api.us5.datadoghq.com`
- **Official documentation:** [Delete Monitor](https://docs.datadoghq.com/api/latest/monitors/#delete-a-monitor)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `monitor_id` | path | `number` | yes | The ID of the monitor to delete. |
| `force` | query | `string` | no | Delete the monitor even if it is referenced by other resources. |
