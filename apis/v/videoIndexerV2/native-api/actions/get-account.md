# Get Account with Video Indexer (V2)

Retrieves an account from Video Indexer (V2).

## Endpoint

- **Method:** `GET`
- **Path:** `/:location/Accounts/:accountId`
- **Base URL:** `https://api.videoindexer.ai`
- **Official documentation:** [Get Account](https://learn.microsoft.com/en-us/connectors/videoindexer-v2/#get-account)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `location` | path | `string` | yes | Indicates the Azure region to which the call should be routed. |
| `accountId` | path | `string` | yes | Video Indexer account ID. |
| `accessToken` | query | `string` | yes | An account access token with read permissions. |
