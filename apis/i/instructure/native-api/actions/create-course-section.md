# Create Course Section with Instructure

Creates a new course section in Instructure Canvas.

## Endpoint

- **Method:** `POST`
- **Path:** `/courses/:course_id/sections`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [Create Course Section](https://developerdocs.instructure.com/services/canvas/resources/sections#method.sections.create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `course_id` | path | `string` | yes | Canvas course ID. |
| `course_section.name` | body | `string` | yes | Name of the section. |
