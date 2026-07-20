# Update Planner Note with Instructure

Updates an existing planner note in Instructure Canvas.

## Endpoint

- **Method:** `PUT`
- **Path:** `/planner_notes/:id`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [Update Planner Note](https://developerdocs.instructure.com/services/canvas/resources/planner)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `details` | body | `string` | no | Details for the planner note. |
| `id` | path | `string` | yes | The Canvas planner note ID. |
| `title` | body | `string` | yes | The title of the planner note. |
| `todo_date` | body | `string` | no | The date and time for the planner note. |
