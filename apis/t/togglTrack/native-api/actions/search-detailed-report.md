# Search Detailed Report with Toggl Track

Finds detailed report time entries in Toggl Track.

## Endpoint

- **Method:** `POST`
- **Path:** `/reports/api/v3/workspace/:workspace_id/search/time_entries`
- **Base URL:** `https://api.track.toggl.com`
- **Official documentation:** [Search Detailed Report](https://engineering.toggl.com/docs/track/reports/detailed_reports/#post-search-time-entries)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspace_id` | path | `list<number>` | yes |
| `start_date` | body | `string` | yes |
| `end_date` | body | `string` | yes |
| `page_size` | body | `number` | no |
| `order_by` | body | `string` | no |
| `order_dir` | body | `string` | no |
| `description` | body | `string` | no |
| `billable` | body | `boolean` | no |
| `grouped` | body | `boolean` | no |
| `hide_amounts` | body | `boolean` | no |
| `enrich_response` | body | `boolean` | no |
