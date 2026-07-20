# List Monitors with Parallel Web Systems

## Endpoint

- **Method:** `GET`
- **Path:** `/v1alpha/monitors`
- **Base URL:** `https://api.parallel.ai`
- **Official documentation:** [List Monitors](https://docs.parallel.ai/api-reference/monitor/list-monitors)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `monitor_id` | query | `string` | no | Monitor ID to start listing after. |
| `limit` | query | `number` | no | Maximum number of monitors to return. |
