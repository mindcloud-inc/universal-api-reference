# Create Source Group with Better Stack Telemetry

Creates a new source group in Better Stack Telemetry.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/source-groups`
- **Base URL:** `https://telemetry.betterstack.com`
- **Official documentation:** [Create Source Group](https://betterstack.com/docs/logs/api/create-a-source-group/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Source group name |
| `team_name` | body | `string` | no | Team that should own the source group |
| `sort_index` | body | `number` | no | Sort order index for the source group |
