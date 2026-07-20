# Get Course Nickname with Instructure

Retrieves a course nickname from Instructure Canvas.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/self/course_nicknames/:course_id`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [Get Course Nickname](https://developerdocs.instructure.com/services/canvas/resources/users#method.coursenicknames.show)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `course_id` | path | `string` | yes | Canvas course ID. |
