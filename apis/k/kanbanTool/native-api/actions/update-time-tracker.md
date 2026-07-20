# Update Time Tracker with Kanban Tool

## Endpoint

- **Method:** `PUT`
- **Path:** `/time_trackers/:time_tracker_id.json`
- **Base URL:** `https://{domain}.kanbantool.com/api/v3`
- **Official documentation:** [Update Time Tracker](https://kanbantool.com/developer/api-v3#updating-time-trackers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `time_tracker_id` | path | `number` | yes | Kanban Tool time tracker ID. |
| `position` | body | `number` | no | Tracker position on the task. |
| `listed` | body | `boolean` | no | Whether the tracker should be shown in the timers list. |
| `started_at` | body | `date` | no | Start timestamp. |
| `ended_at` | body | `date` | no | End timestamp. |
| `highlighted_at` | body | `date` | no | Highlight timestamp. |
