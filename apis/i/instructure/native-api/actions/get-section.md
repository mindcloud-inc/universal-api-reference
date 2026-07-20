# Get Section with Instructure

Retrieves a section from Instructure Canvas.

## Endpoint

- **Method:** `GET`
- **Path:** `/courses/:course_id/sections/:id`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [Get Section](https://developerdocs.instructure.com/services/canvas/resources/sections#method.sections.show)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `course_id` | path | `string` | yes | Canvas course ID. |
| `id` | path | `string` | yes | Canvas section ID. |
