# Update snapshot with Neon

Updates a snapshot in Neon.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/projects/:project_id/snapshots/:snapshot_id`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Update snapshot](https://api-docs.neon.tech/reference/updatesnapshot)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `snapshot_id` | path | `string` | yes | Neon API parameter snapshot_id |
| `snapshot` | body | `object` | yes | Neon API parameter snapshot |
