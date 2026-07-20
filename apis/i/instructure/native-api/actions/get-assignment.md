# Get Assignment with Instructure

Retrieves an assignment from Instructure Canvas.

## Endpoint

- **Method:** `GET`
- **Path:** `/courses/:course_id/assignments/:assignment_id`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [Get Assignment](https://developerdocs.instructure.com/services/canvas/resources/assignments#method.assignments_api.show)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assignment_id` | path | `string` | yes | The Canvas assignment ID. |
| `course_id` | path | `string` | yes | The Canvas course ID. |
