# Search Videos with YouTube

Searches YouTube for videos by default.

## Endpoint

- **Method:** `GET`
- **Path:** `/youtube/v3/search`
- **Base URL:** `https://www.googleapis.com`
- **Official documentation:** [Search Videos](https://developers.google.com/youtube/v3/docs/search/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | no | Search query term. |
| `type` | query | `string` | no | Resource type filter (video, channel, playlist). |
| `channelId` | query | `string` | no | Restrict search to a channel ID. |
| `order` | query | `list<string>` | no | Sort order for search results. Accepted values: `date`, `rating`, `relevance`, `searchSortUnspecified`, `title`, `videoCount`, `viewCount`. |
| `publishedAfter` | query | `date` | no | RFC 3339 timestamp lower bound. |
| `publishedBefore` | query | `date` | no | RFC 3339 timestamp upper bound. |
