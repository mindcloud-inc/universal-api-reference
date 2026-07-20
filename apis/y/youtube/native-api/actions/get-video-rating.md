# Get Video Rating with YouTube

Retrieves the authenticated user's rating for YouTube videos.

## Endpoint

- **Method:** `GET`
- **Path:** `/youtube/v3/videos/getRating`
- **Base URL:** `https://www.googleapis.com`
- **Official documentation:** [Get Video Rating](https://developers.google.com/youtube/v3/docs/videos/getRating)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | yes | One or more YouTube video IDs. Send multiple values as a string separated by `,`. |
| `onBehalfOfContentOwner` | query | `string` | no | Content owner ID when acting on behalf of a CMS user. |
