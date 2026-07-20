# Introspect Token with Skyfire

Retrieves token details from Skyfire.

## Endpoint

- **Method:** `POST`
- **Path:** `/tokens/introspect`
- **Base URL:** `https://api.skyfire.xyz/api/v1`
- **Official documentation:** [Introspect Token](https://docs.skyfire.xyz/reference/introspect-token)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `token` | body | `string` | yes | The complete JWT string as issued to the buyer, not a tokenId. Can be of any token type: kya, pay, or kya-pay. |
