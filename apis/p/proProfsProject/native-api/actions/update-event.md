# Update Event with ProProfs Project

Updates an existing event in ProProfs Project.

## Endpoint

- **Method:** `PUT`
- **Path:** `/events/{{event_id}}`
- **Base URL:** `https://api.projectbubble.com/v2`
- **Official documentation:** [Update Event](https://help.proprofsproject.com/events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `due_date` | body | `string` | no | The updated event due date in yyyymmdd format. |
| `event_id` | path | `string` | yes | The event ID to update. |
| `event_name` | body | `string` | no | The updated event name. |
| `project_id` | body | `string` | no | Attach the updated event to a project. |
| `start_date` | body | `string` | no | The updated event start date in yyyymmdd format. |
