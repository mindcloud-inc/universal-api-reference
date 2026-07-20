# Get Video Thumbnail with Video Indexer (V2)

Retrieves a video thumbnail from Video Indexer (V2).

## Endpoint

- **Method:** `GET`
- **Path:** `/:location/Accounts/:accountId/Videos/:videoId/Thumbnails/:thumbnailId`
- **Base URL:** `https://api.videoindexer.ai`
- **Official documentation:** [Get Video Thumbnail](https://learn.microsoft.com/en-us/connectors/videoindexer-v2/#get-video-thumbnail)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `location` | path | `string` | yes | Indicates the Azure region to which the call should be routed. |
| `accountId` | path | `string` | yes | Video Indexer account ID. |
| `videoId` | path | `string` | yes | The video ID. |
| `thumbnailId` | path | `string` | yes | The thumbnail ID. |
| `accessToken` | query | `string` | yes | An account access token with read permissions. |
