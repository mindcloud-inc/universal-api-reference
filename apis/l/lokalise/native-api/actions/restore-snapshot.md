# Restore Snapshot with Lokalise

Restores a snapshot in a Lokalise project.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:project_id/snapshots/:snapshot_id`
- **Base URL:** `https://api.lokalise.com/api2`
- **Official documentation:** [Restore Snapshot](https://developers.lokalise.com/reference/restore-a-snapshot)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | no | Lokalise project identifier. |
| `snapshot_id` | path | `string` | no | Lokalise snapshot identifier. |
