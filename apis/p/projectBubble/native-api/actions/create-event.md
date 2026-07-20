# Create Event with Project Bubble

Creates a new event in Project Bubble.

## Endpoint

- **Method:** `POST`
- **Path:** `/events`
- **Base URL:** `https://api.projectbubble.com/v2`
- **Official documentation:** [Create Event](https://help.proprofsproject.com/events)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `event_name` | body | `string` | yes |
| `start_date` | body | `string` | yes |
| `due_date` | body | `string` | yes |
| `project_id` | body | `string` | yes |
