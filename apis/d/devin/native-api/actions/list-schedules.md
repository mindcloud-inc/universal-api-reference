# List Schedules with Devin

Retrieves a list of schedules from Devin.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/organizations/:org_id/schedules`
- **Base URL:** `https://api.devin.ai`
- **Official documentation:** [List Schedules](https://docs.devin.ai/api-reference/v3/schedules/organizations-schedules)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum schedules to return. |
| `offset` | query | `number` | no | Zero-based result offset. |
| `org_id` | path | `string` | yes | Devin organization ID. |
