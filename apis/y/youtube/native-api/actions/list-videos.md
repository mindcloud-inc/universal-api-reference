# List Videos with YouTube

Retrieves one or more videos from YouTube.

## Endpoint

- **Method:** `GET`
- **Path:** `/youtube/v3/videos`
- **Base URL:** `https://www.googleapis.com`
- **Official documentation:** [List Videos](https://developers.google.com/youtube/v3/docs/videos/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `part` | query | `string` | yes | Required response parts. |
| `chart` | query | `string` | no | Video chart to retrieve, for example mostPopular. Do not combine with Video ID or My Rating. |
| `id` | query | `string` | no | Comma-separated video IDs. Send multiple values as a string separated by `,`. |
| `myRating` | query | `string` | no | Filter by your rating (like/dislike). |
| `regionCode` | query | `string` | no | ISO 3166-1 alpha-2 region code. Use with Chart requests such as mostPopular. |
| `videoCategoryId` | query | `string` | no | Filter by video category ID. |
