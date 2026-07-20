# Search Summary Report with Toggl Track

Finds summary report time entries in Toggl Track.

## Endpoint

- **Method:** `POST`
- **Path:** `/reports/api/v3/workspace/:workspace_id/summary/time_entries`
- **Base URL:** `https://api.track.toggl.com`
- **Official documentation:** [Search Summary Report](https://engineering.toggl.com/docs/track/reports/summary_reports/#post-search-time-entries)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspace_id` | path | `list<number>` | yes |
| `start_date` | body | `string` | yes |
| `end_date` | body | `string` | yes |
| `grouping` | body | `string` | no |
| `sub_grouping` | body | `string` | no |
| `description` | body | `string` | no |
| `billable` | body | `boolean` | no |
