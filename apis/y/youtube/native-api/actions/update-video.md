# Update Video with YouTube

Updates an existing video in YouTube.

## Endpoint

- **Method:** `PUT`
- **Path:** `/youtube/v3/videos`
- **Base URL:** `https://www.googleapis.com`
- **Official documentation:** [Update Video](https://developers.google.com/youtube/v3/docs/videos/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `part` | query | `string` | yes | Send multiple values as a string separated by `,`. |
| `id` | body | `string` | yes | — |
| `snippet.title` | body | `string` | no | — |
| `snippet.description` | body | `string` | no | — |
| `status.privacyStatus` | body | `string` | no | — |
| `snippet.tags[]` | body | `array<string>` | no | — |
| `localizations` | body | `object` | no | — |
| `onBehalfOfContentOwner` | query | `string` | no | — |
