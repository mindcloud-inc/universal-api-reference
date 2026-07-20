# List Videos with Video Indexer (V2)

Retrieves videos from Video Indexer (V2).

## Endpoint

- **Method:** `GET`
- **Path:** `/:location/Accounts/:accountId/Videos`
- **Base URL:** `https://api.videoindexer.ai`
- **Official documentation:** [List Videos](https://learn.microsoft.com/en-us/connectors/videoindexer-v2/#list-videos)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `location` | path | `string` | yes | Indicates the Azure region to which the call should be routed. |
| `accountId` | path | `string` | yes | Video Indexer account ID. |
| `accessToken` | query | `string` | yes | An account access token with read permissions. |
