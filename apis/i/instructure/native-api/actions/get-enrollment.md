# Get Enrollment with Instructure

Retrieves an enrollment from Instructure Canvas.

## Endpoint

- **Method:** `GET`
- **Path:** `/courses/:course_id/enrollments/:enrollment_id`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [Get Enrollment](https://developerdocs.instructure.com/services/canvas/resources/enrollments#method.enrollments_api.show)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `course_id` | path | `string` | yes | The Canvas course ID. |
| `enrollment_id` | path | `string` | yes | The Canvas enrollment ID. |
