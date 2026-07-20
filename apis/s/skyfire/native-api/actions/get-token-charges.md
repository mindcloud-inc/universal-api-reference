# Get Token Charges with Skyfire

Retrieves token charges from Skyfire.

## Endpoint

- **Method:** `GET`
- **Path:** `/tokens/:tokenId/charges`
- **Base URL:** `https://api.skyfire.xyz/api/v1`
- **Official documentation:** [Get Token Charges](https://docs.skyfire.xyz/reference/get-token-charges)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tokenId` | path | `string` | yes | The ID of the pay or kya-pay token. This is the value of the jti claim in the token body. |
