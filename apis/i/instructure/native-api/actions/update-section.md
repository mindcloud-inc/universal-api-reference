# Update Section with Instructure

Updates an existing section in Instructure Canvas.

## Endpoint

- **Method:** `PUT`
- **Path:** `/sections/:id`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [Update Section](https://developerdocs.instructure.com/services/canvas/resources/sections#method.sections.update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `course_section.name` | body | `string` | no | Updated section name. |
| `id` | path | `string` | yes | Canvas section ID. |
