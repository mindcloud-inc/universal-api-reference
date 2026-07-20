# Upload Video with YouTube

Uploads a new video to YouTube.

## Endpoint

- **Method:** `POST`
- **Path:** `/upload/youtube/v3/videos`
- **Base URL:** `https://www.googleapis.com`
- **Official documentation:** [Upload Video](https://developers.google.com/youtube/v3/docs/videos/insert)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `part` | query | `string` | yes | Send multiple values as a string separated by `,`. |
| `snippet.title` | body | `string` | yes | — |
| `snippet.description` | body | `string` | no | — |
| `snippet.categoryId` | body | `string` | yes | YouTube video category ID. Required when the upload includes the snippet part. |
| `status.privacyStatus` | body | `string` | no | — |
| `snippet.tags[]` | body | `array<string>` | no | — |
| `mediaFile` | body | `file` | yes | Binary video media file to upload. |
| `notifySubscribers` | query | `boolean` | no | — |
| `autoLevels` | query | `boolean` | no | — |
| `stabilize` | query | `boolean` | no | — |
| `onBehalfOfContentOwner` | query | `string` | no | — |
| `onBehalfOfContentOwnerChannel` | query | `string` | no | — |
