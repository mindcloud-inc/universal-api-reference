# Update Video Transcript with Video Indexer (V2)

Updates a video's transcript in Video Indexer (V2).

## Endpoint

- **Method:** `PUT`
- **Path:** `/:location/Accounts/:accountId/Videos/:videoId/Index/Transcript`
- **Base URL:** `https://api.videoindexer.ai`
- **Official documentation:** [Update Video Transcript](https://learn.microsoft.com/en-us/connectors/videoindexer-v2/#update-video-transcript)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `text/vtt` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `location` | path | `string` | yes | Indicates the Azure region to which the call should be routed. |
| `accountId` | path | `string` | yes | Video Indexer account ID. |
| `videoId` | path | `string` | yes | The video ID. |
| `accessToken` | query | `string` | yes | An account access token. |
| `language` | query | `string` | yes | The language of the captions. |
| `content` | body | `string` | yes | The transcript to update. |
