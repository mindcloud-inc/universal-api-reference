# Re-Index Video with Video Indexer (V2)

Re-indexes a video in Video Indexer (V2).

## Endpoint

- **Method:** `PUT`
- **Path:** `/:location/Accounts/:accountId/Videos/:videoId/Index`
- **Base URL:** `https://api.videoindexer.ai`
- **Official documentation:** [Re-Index Video](https://learn.microsoft.com/en-us/connectors/videoindexer-v2/#re-index-video)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `location` | path | `string` | yes | Indicates the Azure region to which the call should be routed. |
| `accountId` | path | `string` | yes | Video Indexer account ID. |
| `videoId` | path | `string` | yes | The video ID. |
| `accessToken` | query | `string` | yes | An account access token with write permissions. |
| `indexingPreset` | query | `string` | no | The indexing preset to use. |
| `streamingPreset` | query | `string` | no | The streaming preset to use. |
| `sourceLanguage` | query | `string` | no | The source language of the video. |
