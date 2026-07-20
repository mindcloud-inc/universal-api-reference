# Delete Snapshot with Lokalise

Deletes a snapshot from a Lokalise project.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/projects/:project_id/snapshots/:snapshot_id`
- **Base URL:** `https://api.lokalise.com/api2`
- **Official documentation:** [Delete Snapshot](https://developers.lokalise.com/reference/delete-a-snapshot)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | no | Lokalise project identifier. |
| `snapshot_id` | path | `string` | no | Lokalise snapshot identifier. |
