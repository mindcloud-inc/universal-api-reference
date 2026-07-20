# Update backup schedule with Neon

Updates a backup schedule in Neon.

## Endpoint

- **Method:** `PUT`
- **Path:** `/projects/:project_id/branches/:branch_id/backup_schedule`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Update backup schedule](https://api-docs.neon.tech/reference/setsnapshotschedule)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `branch_id` | path | `string` | yes | Neon API parameter branch_id |
| `schedule[]` | body | `array<object>` | yes | Neon API parameter schedule |
