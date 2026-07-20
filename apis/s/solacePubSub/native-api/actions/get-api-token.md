# Get API Token with Solace PubSub+

Retrieves an API token from Solace PubSub+.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/platform/apiTokens/{tokenId}`
- **Base URL:** `https://api.solace.cloud`
- **Official documentation:** [Get API Token](https://api.solace.dev/cloud/reference/gettoken)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tokenId` | path | `string` | yes | Unique Solace Cloud API token identifier. |
