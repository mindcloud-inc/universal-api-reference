# Update Folder with Instructure

Updates an existing folder in Instructure Canvas.

## Endpoint

- **Method:** `PUT`
- **Path:** `/folders/:folder_id`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [Update Folder](https://developerdocs.instructure.com/services/canvas/resources/files#method.folders.update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folder_id` | path | `string` | yes | The Canvas folder ID. |
| `name` | body | `string` | no | The updated folder name. |
