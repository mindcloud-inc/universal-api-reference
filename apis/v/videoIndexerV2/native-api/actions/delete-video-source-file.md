# Delete Video Source File with Video Indexer (V2)

Deletes a video's source file from Video Indexer (V2).

## Endpoint

- **Method:** `DELETE`
- **Path:** `/:location/Accounts/:accountId/Videos/:videoId/SourceFile`
- **Base URL:** `https://api.videoindexer.ai`
- **Official documentation:** [Delete Video Source File](https://learn.microsoft.com/en-us/connectors/videoindexer-v2/#delete-video-source-file)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `location` | path | `string` | yes | Indicates the Azure region to which the call should be routed. |
| `accountId` | path | `string` | yes | Video Indexer account ID. |
| `videoId` | path | `string` | yes | The video ID. |
| `accessToken` | query | `string` | yes | An account access token with write permissions. |
