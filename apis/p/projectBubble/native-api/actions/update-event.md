# Update Event with Project Bubble

Updates an existing event in Project Bubble.

## Endpoint

- **Method:** `PUT`
- **Path:** `/events/:event_id`
- **Base URL:** `https://api.projectbubble.com/v2`
- **Official documentation:** [Update Event](https://help.proprofsproject.com/events)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `event_id` | path | `string` | yes |
| `start_date` | body | `string` | yes |
| `due_date` | body | `string` | yes |
| `project_id` | body | `string` | yes |
| `event_name` | body | `string` | no |
