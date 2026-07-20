# Delete Folder with Instructure

Deletes a folder from Instructure Canvas.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/folders/:folder_id`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [Delete Folder](https://developerdocs.instructure.com/services/canvas/resources/files#method.folders.api_destroy)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folder_id` | path | `string` | yes | The Canvas folder ID. |
