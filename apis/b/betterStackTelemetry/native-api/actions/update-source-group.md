# Update Source Group with Better Stack Telemetry

Updates an existing source group in Better Stack Telemetry.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/source-groups/:source_group_id`
- **Base URL:** `https://telemetry.betterstack.com`
- **Official documentation:** [Update Source Group](https://betterstack.com/docs/logs/api/updating-a-source-group/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source_group_id` | path | `string` | yes | ID of the source group to update |
| `name` | body | `string` | no | Source group name |
| `sort_index` | body | `number` | no | Sort order index for the source group |
