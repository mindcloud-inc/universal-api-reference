# Remove Course Nickname with Instructure

Deletes a course nickname from Instructure Canvas.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/users/self/course_nicknames/:course_id`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [Remove Course Nickname](https://developerdocs.instructure.com/services/canvas/resources/users#method.coursenicknames.delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `course_id` | path | `string` | yes | Canvas course ID. |
