# Add Comment to Issue Timeline with SafetyCulture

Creates an issue timeline comment in SafetyCulture.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks/v1/timeline/comments`
- **Base URL:** `https://api.safetyculture.io`
- **Official documentation:** [Add Comment to Issue Timeline](https://developer.safetyculture.com/reference/timelineservice_addcomment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | body | `string` | yes | Required. The UUID for the task the comment is being added to. |
| `comment` | body | `string` | yes | Required. The content of the comment. |
| `created_at` | body | `date` | no | Optional. Date/time this comment was added. |
| `event_id` | body | `string` | no | Optional. The unique identifier for the event. This will be auto-generated if omitted. |
