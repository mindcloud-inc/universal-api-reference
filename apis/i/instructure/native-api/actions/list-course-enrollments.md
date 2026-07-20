# List Course Enrollments with Instructure

Retrieves course enrollments from Instructure Canvas.

## Endpoint

- **Method:** `GET`
- **Path:** `/courses/:course_id/enrollments`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [List Course Enrollments](https://developerdocs.instructure.com/services/canvas/resources/enrollments#method.enrollments_api.index)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `course_id` | path | `string` | yes | The Canvas course ID. |
