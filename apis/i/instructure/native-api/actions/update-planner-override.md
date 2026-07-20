# Update Planner Override with Instructure

Updates an existing planner override in Instructure Canvas.

## Endpoint

- **Method:** `PUT`
- **Path:** `/planner/overrides/:id`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [Update Planner Override](https://developerdocs.instructure.com/services/canvas/resources/planner)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dismissed` | body | `string` | no | Whether the plannable item is dismissed. |
| `id` | path | `string` | yes | The Canvas planner override ID. |
| `marked_complete` | body | `string` | no | Whether the plannable item is marked complete. |
