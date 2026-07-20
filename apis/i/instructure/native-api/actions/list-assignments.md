# List Assignments with Instructure

Retrieves assignments from Instructure Canvas.

## Endpoint

- **Method:** `GET`
- **Path:** `/courses/:course_id/assignments`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [List Assignments](https://developerdocs.instructure.com/services/canvas/resources/assignments#method.assignments_api.index)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `course_id` | path | `string` | yes | The Canvas course ID. |
