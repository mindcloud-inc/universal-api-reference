# Update File with Instructure

Updates a file in Instructure Canvas.

## Endpoint

- **Method:** `PUT`
- **Path:** `/files/:id`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [Update File](https://developerdocs.instructure.com/services/canvas/resources/files#method.files.api_update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `display_name` | body | `string` | no | Updated display name for the file. |
| `id` | path | `string` | yes | Canvas file ID. |
