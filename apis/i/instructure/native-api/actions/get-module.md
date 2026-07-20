# Get Module with Instructure

Retrieves a module from Instructure Canvas.

## Endpoint

- **Method:** `GET`
- **Path:** `/courses/:course_id/modules/:module_id`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [Get Module](https://developerdocs.instructure.com/services/canvas/resources/modules#method.context_modules_api.show)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `course_id` | path | `string` | yes | The Canvas course ID. |
| `module_id` | path | `string` | yes | The Canvas module ID. |
