# Remove Source Group with Better Stack Telemetry

Deletes an existing source group from Better Stack Telemetry.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v1/source-groups/:source_group_id`
- **Base URL:** `https://telemetry.betterstack.com`
- **Official documentation:** [Remove Source Group](https://betterstack.com/docs/logs/api/deleting-an-existing-source-group/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source_group_id` | path | `string` | yes | ID of the source group to remove |
