# Upload Video And Index with Video Indexer (V2)

Uploads and indexes a video in Video Indexer (V2).

## Endpoint

- **Method:** `POST`
- **Path:** `/:location/Accounts/:accountId/Videos`
- **Base URL:** `https://api.videoindexer.ai`
- **Official documentation:** [Upload Video And Index](https://learn.microsoft.com/en-us/connectors/videoindexer-v2/#upload-video-and-index)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `location` | path | `string` | yes | Azure region to route the call to. |
| `accountId` | path | `string` | yes | Video Indexer account ID. |
| `accessToken` | query | `string` | yes | Account access token with write permissions. |
| `name` | query | `string` | yes | The title of the video. |
| `videoUrl` | query | `string` | yes | A public URL of the video or audio file to index. |
| `externalId` | query | `string` | no | An external ID associated with the uploaded video. |
| `privacy` | query | `string` | no | The video privacy. |
