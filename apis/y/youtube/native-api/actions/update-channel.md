# Update Channel with YouTube

Updates an existing channel in YouTube.

## Endpoint

- **Method:** `PUT`
- **Path:** `/youtube/v3/channels`
- **Base URL:** `https://www.googleapis.com`
- **Official documentation:** [Update Channel](https://developers.google.com/youtube/v3/docs/channels/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `part` | query | `string` | yes | Send multiple values as a string separated by `,`. |
| `id` | body | `string` | yes | — |
| `brandingSettings` | body | `object` | no | — |
| `invideoPromotion` | body | `object` | no | — |
| `onBehalfOfContentOwner` | query | `string` | no | — |
