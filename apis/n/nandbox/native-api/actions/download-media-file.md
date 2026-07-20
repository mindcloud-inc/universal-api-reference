# Download Media File with nandbox

Retrieves a media file from nandbox by media ID.

## Endpoint

- **Method:** `GET`
- **Path:** `{{mediaId}}`
- **Base URL:** `{downloadServer}/`
- **Official documentation:** [Download Media File](https://developer.nandbox.com/media/downloading-media-files)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `media_id` | path | `string` | yes | Unique media identifier returned by nandbox for a previously uploaded file. |
