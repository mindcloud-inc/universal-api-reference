# Get Account Access Token with Video Indexer (V2)

Retrieves an account access token from Video Indexer (V2).

## Endpoint

- **Method:** `GET`
- **Path:** `/Auth/:location/Accounts/:accountId/AccessToken`
- **Base URL:** `https://api.videoindexer.ai`
- **Official documentation:** [Get Account Access Token](https://learn.microsoft.com/en-us/connectors/videoindexer-v2/#get-account-access-token)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `location` | path | `string` | yes | Azure region to route the call to, such as Trial for trial accounts. |
| `accountId` | path | `string` | yes | Video Indexer account ID. |
| `allowEdit` | query | `boolean` | yes | Whether the returned account access token can be used for write operations. |
