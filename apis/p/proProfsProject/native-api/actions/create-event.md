# Create Event with ProProfs Project

Creates a new event in ProProfs Project.

## Endpoint

- **Method:** `POST`
- **Path:** `/events`
- **Base URL:** `https://api.projectbubble.com/v2`
- **Official documentation:** [Create Event](https://help.proprofsproject.com/events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `due_date` | body | `string` | yes | The event due date in yyyymmdd format. |
| `event_name` | body | `string` | yes | The event name. |
| `project_id` | body | `string` | no | Attach the event to a project. |
| `start_date` | body | `string` | yes | The event start date in yyyymmdd format. |
