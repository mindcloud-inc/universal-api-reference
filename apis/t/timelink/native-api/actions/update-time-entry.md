# Update Time Entry with Timelink

Updates an existing time entry in Timelink.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/timeEntries/:id`
- **Base URL:** `https://api.timelink.io/api/v1`
- **Official documentation:** [Update Time Entry](https://api.timelink.io/documentation#/Time%20Entries/patch_api_v1_timeEntries__id_)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `description` | body | `string` | no |
| `ended_at` | body | `string` | no |
