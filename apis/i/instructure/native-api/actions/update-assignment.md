# Update Assignment with Instructure

Updates an existing assignment in Instructure Canvas.

## Endpoint

- **Method:** `PUT`
- **Path:** `/courses/:course_id/assignments/:assignment_id`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [Update Assignment](https://developerdocs.instructure.com/services/canvas/resources/assignments#method.assignments_api.update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `course_id` | path | `string` | yes | The Canvas course ID. |
| `assignment_id` | path | `string` | yes | The Canvas assignment ID. |
| `assignment[name]` | body | `string` | no | Assignment name. |
| `assignment[description]` | body | `string` | no | Assignment description. |
| `assignment[due_at]` | body | `string` | no | Assignment due timestamp. |
| `assignment[points_possible]` | body | `number` | no | Maximum points possible. |
