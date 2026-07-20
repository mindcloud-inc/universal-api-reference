# List Captions with YouTube

Retrieves caption tracks for a YouTube video.

## Endpoint

- **Method:** `GET`
- **Path:** `/youtube/v3/captions`
- **Base URL:** `https://www.googleapis.com`
- **Official documentation:** [List Captions](https://developers.google.com/youtube/v3/docs/captions/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `part` | query | `string` | yes | Send multiple values as a string separated by `,`. |
| `videoId` | query | `string` | yes | — |
| `id` | query | `string` | no | Send multiple values as a string separated by `,`. |
| `onBehalfOf` | query | `string` | no | — |
| `onBehalfOfContentOwner` | query | `string` | no | — |
