# Update Face Name with Video Indexer (V2)

Updates a face name in Video Indexer (V2).

## Endpoint

- **Method:** `PUT`
- **Path:** `/:location/Accounts/:accountId/Videos/:videoId/Index/Faces/:faceId`
- **Base URL:** `https://api.videoindexer.ai`
- **Official documentation:** [Update Face Name](https://learn.microsoft.com/en-us/connectors/videoindexer-v2/#update-face-name)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `location` | path | `string` | yes | Indicates the Azure region to which the call should be routed. |
| `accountId` | path | `string` | yes | Video Indexer account ID. |
| `videoId` | path | `string` | yes | The video ID. |
| `faceId` | path | `number` | yes | The face ID. |
| `accessToken` | query | `string` | yes | An account access token with write permissions. |
| `newName` | query | `string` | yes | A new name for the face. |
