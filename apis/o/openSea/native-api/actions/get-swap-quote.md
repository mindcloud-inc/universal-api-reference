# Get Swap Quote with OpenSea

Retrieves a swap quote from OpenSea.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/swap/quote`
- **Base URL:** `https://api.opensea.io`
- **Official documentation:** [Get Swap Quote](https://docs.opensea.io/reference/get_swap_quote)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from_chain` | query | `string` | yes | Chain of the token to swap from |
| `from_address` | query | `string` | yes | Contract address of the token to swap from |
| `to_chain` | query | `string` | yes | Chain of the token to swap to |
| `to_address` | query | `string` | yes | Contract address of the token to swap to |
| `quantity` | query | `string` | yes | Amount to swap in the smallest unit of the token (e.g. wei for ETH) |
| `address` | query | `string` | yes | Wallet address executing the swap |
| `slippage` | query | `number` | no | Slippage tolerance (0.0 to 0.5, default: 0.01) |
| `recipient` | query | `string` | no | Recipient address (defaults to sender address) |
