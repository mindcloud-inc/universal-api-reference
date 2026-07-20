# Create Folder with Instructure

Creates a new folder in Instructure Canvas.

## Endpoint

- **Method:** `POST`
- **Path:** `/folders/:parent_folder_id/folders`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [Create Folder](https://developerdocs.instructure.com/services/canvas/resources/files#method.folders.create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The name of the new folder. |
| `parent_folder_id` | path | `string` | yes | The Canvas parent folder ID. |
