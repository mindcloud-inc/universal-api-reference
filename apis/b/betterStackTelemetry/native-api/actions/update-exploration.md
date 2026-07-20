# Update Exploration with Better Stack Telemetry

Updates an existing exploration in Better Stack Telemetry.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v2/explorations/:id`
- **Base URL:** `https://telemetry.betterstack.com`
- **Official documentation:** [Update Exploration](https://betterstack.com/docs/logs/api/explorations/update/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The ID of the exploration to update. |
| `name` | body | `string` | no | New exploration name. |
| `date_range_from` | body | `string` | no | Start of the exploration date range. |
| `date_range_to` | body | `string` | no | End of the exploration date range. |
| `exploration_group_id` | body | `number` | no | Exploration group ID for the exploration. |
| `chart` | body | `object` | no | Chart configuration object. |
| `queries[]` | body | `array` | no | Array of exploration queries. |
| `variables[]` | body | `array` | no | Array of exploration variables. |
