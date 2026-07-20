# Get Course with Instructure

Retrieves a course from Instructure Canvas.

## Endpoint

- **Method:** `GET`
- **Path:** `/courses/:course_id`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [Get Course](https://developerdocs.instructure.com/services/canvas/resources/courses#method.courses.show)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `course_id` | path | `string` | yes | The Canvas course ID. |
