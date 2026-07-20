# Search Videos with Video Indexer (V2)

Finds videos in Video Indexer (V2) by query.

## Endpoint

- **Method:** `GET`
- **Path:** `/:location/Accounts/:accountId/Videos/Search`
- **Base URL:** `https://api.videoindexer.ai`
- **Official documentation:** [Search Videos](https://learn.microsoft.com/en-us/connectors/videoindexer-v2/#search-videos)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `location` | path | `string` | yes | Indicates the Azure region to which the call should be routed. |
| `accountId` | path | `string` | yes | Video Indexer account ID. |
| `accessToken` | query | `string` | yes | An account access token with read permissions. |
| `externalId` | query | `string` | no | An external ID associated with a video. |
| `query` | query | `string` | no | Free text to search for. |
| `privacy` | query | `string` | no | The video privacy. |
