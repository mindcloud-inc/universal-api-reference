# List Folder Files with Instructure

Retrieves files in a folder from Instructure Canvas.

## Endpoint

- **Method:** `GET`
- **Path:** `/folders/:folder_id/files`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [List Folder Files](https://developerdocs.instructure.com/services/canvas/resources/files#method.files.api_index)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folder_id` | path | `string` | yes | The Canvas folder ID. |
