# Get Video Index with Video Indexer (V2)

Retrieves a video's index from Video Indexer (V2).

## Endpoint

- **Method:** `GET`
- **Path:** `/:location/Accounts/:accountId/Videos/:videoId/Index`
- **Base URL:** `https://api.videoindexer.ai`
- **Official documentation:** [Get Video Index](https://learn.microsoft.com/en-us/connectors/videoindexer-v2/#get-video-index)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `location` | path | `string` | yes | Indicates the Azure region to which the call should be routed. |
| `accountId` | path | `string` | yes | Video Indexer account ID. |
| `videoId` | path | `string` | yes | The video ID. |
| `accessToken` | query | `string` | yes | An account access token with read permissions. |
| `language` | query | `string` | no | The language of the captions. |
