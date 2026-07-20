# List Comment Threads with YouTube

Retrieves comment threads for YouTube videos or channels.

## Endpoint

- **Method:** `GET`
- **Path:** `/youtube/v3/commentThreads`
- **Base URL:** `https://www.googleapis.com`
- **Official documentation:** [List Comment Threads](https://developers.google.com/youtube/v3/docs/commentThreads/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `part` | query | `string` | yes | Comma-separated commentThread resource parts to include. |
| `allThreadsRelatedToChannelId` | query | `string` | no | Retrieve threads associated with a specific channel ID. |
| `videoId` | query | `string` | no | Retrieve threads for a specific video. |
| `id` | query | `string` | no | Comma-separated list of comment thread IDs. |
| `moderationStatus` | query | `string` | no | Restrict results by moderation status. |
| `order` | query | `list<string>` | no | Sort order for returned threads. Accepted values: `orderUnspecified`, `relevance`, `time`. |
| `searchTerms` | query | `string` | no | Search text to match comment threads. |
| `textFormat` | query | `string` | no | Comment text format, html or plainText. |
