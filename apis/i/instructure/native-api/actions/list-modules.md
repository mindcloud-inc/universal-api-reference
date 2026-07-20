# List Modules with Instructure

Retrieves modules from Instructure Canvas.

## Endpoint

- **Method:** `GET`
- **Path:** `/courses/:course_id/modules`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [List Modules](https://developerdocs.instructure.com/services/canvas/resources/modules#method.context_modules_api.index)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `course_id` | path | `string` | yes | The Canvas course ID. |
