# Create Planner Note with Instructure

Creates a new planner note in Instructure Canvas.

## Endpoint

- **Method:** `POST`
- **Path:** `/planner_notes`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [Create Planner Note](https://developerdocs.instructure.com/services/canvas/resources/planner)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `details` | body | `string` | no | Details for the planner note. |
| `title` | body | `string` | yes | The title of the planner note. |
| `todo_date` | body | `string` | no | The date and time for the planner note. |
