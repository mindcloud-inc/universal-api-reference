# Get File with Instructure

Retrieves a file from Instructure Canvas.

## Endpoint

- **Method:** `GET`
- **Path:** `/files/:file_id`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [Get File](https://developerdocs.instructure.com/services/canvas/resources/files#method.files.api_show)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_id` | path | `string` | yes | The Canvas file ID. |
