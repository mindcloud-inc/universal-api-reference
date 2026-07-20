# Get Video ID By External ID with Video Indexer (V2)

Retrieves a video ID from an external ID in Video Indexer (V2).

## Endpoint

- **Method:** `GET`
- **Path:** `/:location/Accounts/:accountId/Videos/GetIdByExternalId`
- **Base URL:** `https://api.videoindexer.ai`
- **Official documentation:** [Get Video ID By External ID](https://learn.microsoft.com/en-us/connectors/videoindexer-v2/#get-video-id-by-external-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `location` | path | `string` | yes | Indicates the Azure region to which the call should be routed. |
| `accountId` | path | `string` | yes | Video Indexer account ID. |
| `externalId` | query | `string` | yes | The external ID. |
| `accessToken` | query | `string` | yes | An account access token with read permissions. |
