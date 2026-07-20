# Set Course Nickname with Instructure

Sets a course nickname in Instructure Canvas.

## Endpoint

- **Method:** `PUT`
- **Path:** `/users/self/course_nicknames/:course_id`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [Set Course Nickname](https://developerdocs.instructure.com/services/canvas/resources/users#method.coursenicknames.update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `course_id` | path | `string` | yes | Canvas course ID. |
| `nickname` | body | `string` | yes | Nickname to store for the course. |
