# Delete snapshot with Neon

Deletes a snapshot from Neon.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/projects/:project_id/snapshots/:snapshot_id`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Delete snapshot](https://api-docs.neon.tech/reference/deletesnapshot)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `snapshot_id` | path | `string` | yes | Neon API parameter snapshot_id |
