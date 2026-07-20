# List Module Items with Instructure

Retrieves module items from Instructure Canvas.

## Endpoint

- **Method:** `GET`
- **Path:** `/courses/:course_id/modules/:module_id/items`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [List Module Items](https://developerdocs.instructure.com/services/canvas/resources/modules#method.context_module_items_api.index)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `course_id` | path | `string` | yes | The Canvas course ID. |
| `module_id` | path | `string` | yes | The Canvas module ID. |
