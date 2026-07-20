# Set Thumbnail with YouTube

Sets a custom thumbnail for a YouTube video.

## Endpoint

- **Method:** `POST`
- **Path:** `/upload/youtube/v3/thumbnails/set`
- **Base URL:** `https://www.googleapis.com`
- **Official documentation:** [Set Thumbnail](https://developers.google.com/youtube/v3/docs/thumbnails/set)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `videoId` | query | `string` | yes | ID of the video for which the custom thumbnail is being provided. |
| `image` | body | `file` | yes | Binary image file to upload as the custom thumbnail. |
| `onBehalfOfContentOwner` | query | `string` | no | Content owner ID when acting on behalf of a CMS user. |
