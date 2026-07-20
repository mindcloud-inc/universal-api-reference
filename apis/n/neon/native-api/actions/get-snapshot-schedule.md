# View backup schedule with Neon

Retrieves backup schedule from Neon.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/branches/:branch_id/backup_schedule`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [View backup schedule](https://api-docs.neon.tech/reference/getsnapshotschedule)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `branch_id` | path | `string` | yes | Neon API parameter branch_id |
