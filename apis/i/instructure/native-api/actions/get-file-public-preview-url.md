# Get File Public Preview URL with Instructure

Retrieves a file public preview URL from Instructure Canvas.

## Endpoint

- **Method:** `GET`
- **Path:** `/files/:id/public_url`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [Get File Public Preview URL](https://developerdocs.instructure.com/services/canvas/resources/files#method.files.public_url)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Canvas file ID. |
