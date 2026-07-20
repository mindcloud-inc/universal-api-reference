# Get Video Captions with Video Indexer (V2)

Retrieves video captions from Video Indexer (V2).

## Endpoint

- **Method:** `GET`
- **Path:** `/:location/Accounts/:accountId/Videos/:videoId/Captions`
- **Base URL:** `https://api.videoindexer.ai`
- **Official documentation:** [Get Video Captions](https://learn.microsoft.com/en-us/connectors/videoindexer-v2/#get-video-captions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `location` | path | `string` | yes | Indicates the Azure region to which the call should be routed. |
| `accountId` | path | `string` | yes | Video Indexer account ID. |
| `videoId` | path | `string` | yes | The video ID. |
| `accessToken` | query | `string` | yes | An account access token with read permissions. |
| `format` | query | `string` | yes | The captions format, for example vtt. |
| `language` | query | `string` | no | The language of the captions. |
