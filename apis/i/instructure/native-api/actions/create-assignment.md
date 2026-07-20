# Create Assignment with Instructure

Creates a new assignment in Instructure Canvas.

## Endpoint

- **Method:** `POST`
- **Path:** `/courses/:course_id/assignments`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [Create Assignment](https://developerdocs.instructure.com/services/canvas/resources/assignments#method.assignments_api.create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `course_id` | path | `string` | yes | The Canvas course ID. |
| `assignment[name]` | body | `string` | yes | Assignment name. |
| `assignment[description]` | body | `string` | no | Assignment description. |
| `assignment[due_at]` | body | `string` | no | Assignment due timestamp. |
| `assignment[points_possible]` | body | `number` | no | Maximum points possible. |
