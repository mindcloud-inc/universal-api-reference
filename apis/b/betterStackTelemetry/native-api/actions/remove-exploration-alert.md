# Remove Exploration Alert with Better Stack Telemetry

Deletes an existing exploration alert from Better Stack Telemetry.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v2/explorations/:exploration_id/alerts/:id`
- **Base URL:** `https://telemetry.betterstack.com`
- **Official documentation:** [Remove Exploration Alert](https://betterstack.com/docs/logs/api/alerts/delete/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `exploration_id` | path | `string` | yes | The ID of the exploration that owns the alert. |
| `id` | path | `string` | yes | The ID of the alert to remove. |
