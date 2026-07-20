# Delete Assignment with Instructure

Deletes an assignment from Instructure Canvas.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/courses/:course_id/assignments/:assignment_id`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [Delete Assignment](https://developerdocs.instructure.com/services/canvas/resources/assignments#method.assignments.destroy)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assignment_id` | path | `string` | yes | The Canvas assignment ID. |
| `course_id` | path | `string` | yes | The Canvas course ID. |
