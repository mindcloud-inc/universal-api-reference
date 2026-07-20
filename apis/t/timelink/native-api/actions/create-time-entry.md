# Create Time Entry with Timelink

Creates a time entry in Timelink.

## Endpoint

- **Method:** `POST`
- **Path:** `/timeEntries`
- **Base URL:** `https://api.timelink.io/api/v1`
- **Official documentation:** [Create Time Entry](https://api.timelink.io/documentation#/Time%20Entries/post_api_v1_timeEntries)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `user_id` | body | `string` | yes |
| `client_id` | body | `string` | yes |
| `started_at` | body | `string` | yes |
| `ended_at` | body | `string` | yes |
| `description` | body | `string` | no |
| `ext_tool_id` | body | `string` | no |
