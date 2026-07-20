# Create Time Entry with Timing

Creates a new time entry in Timing.

## Endpoint

- **Method:** `POST`
- **Path:** `/time-entries`
- **Base URL:** `https://web.timingapp.com/api/v1`
- **Official documentation:** [Create Time Entry](https://web.timingapp.com/docs/#time-entries-POSTapi-v1-time-entries)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `start_date` | body | `string` | yes |
| `end_date` | body | `string` | yes |
| `project` | body | `string` | no |
| `title` | body | `string` | no |
