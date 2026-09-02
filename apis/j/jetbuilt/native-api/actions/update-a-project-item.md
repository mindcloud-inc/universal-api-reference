# Update a Project Item with Jetbuilt

## Endpoint

- **Method:** `PUT`
- **Path:** `projects/:projectId/items/:id`
- **Base URL:** `https://app.jetbuilt.com/api/`

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `projectId` | path | `number` | yes |
| `id` | path | `number` | yes |
| `quantity_per_room` | body | `string` | no |
