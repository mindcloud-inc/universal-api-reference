# Create Time Tracker with Kanban Tool

## Endpoint

- **Method:** `POST`
- **Path:** `/time_trackers.json`
- **Base URL:** `https://{domain}.kanbantool.com/api/v3`
- **Official documentation:** [Create Time Tracker](https://kanbantool.com/developer/api-v3#creating-time-trackers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `board_id` | body | `number` | yes | Board where the time tracker should live. |
| `task_id` | body | `number` | yes | Task linked to the time tracker. |
| `position` | body | `number` | no | Tracker position on the task. |
| `listed` | body | `boolean` | no | Whether the tracker should be shown in the timers list. |
| `started_at` | body | `date` | no | Start timestamp. |
| `ended_at` | body | `date` | no | End timestamp. |
| `highlighted_at` | body | `date` | no | Highlight timestamp. |
