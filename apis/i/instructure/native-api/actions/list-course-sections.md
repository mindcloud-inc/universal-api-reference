# List Course Sections with Instructure

Retrieves course sections from Instructure Canvas.

## Endpoint

- **Method:** `GET`
- **Path:** `/courses/:course_id/sections`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [List Course Sections](https://developerdocs.instructure.com/services/canvas/resources/sections#method.sections.index)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `course_id` | path | `string` | yes | Canvas course ID. |
