# Create Planner Override with Instructure

Creates a new planner override in Instructure Canvas.

## Endpoint

- **Method:** `POST`
- **Path:** `/planner/overrides`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [Create Planner Override](https://developerdocs.instructure.com/services/canvas/resources/planner)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dismissed` | body | `string` | no | Whether the plannable item is dismissed. |
| `marked_complete` | body | `string` | no | Whether the plannable item is marked complete. |
| `plannable_id` | body | `string` | yes | The ID of the plannable object. |
| `plannable_type` | body | `string` | yes | The type of object being overridden, such as PlannerNote. |
