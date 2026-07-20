# Get Token Balances By Wallet with OpenSea

Retrieves token balances for an OpenSea account.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/account/{address}/tokens`
- **Base URL:** `https://api.opensea.io`
- **Official documentation:** [Get Token Balances By Wallet](https://docs.opensea.io/reference/get_token_balances_by_account)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | path | `string` | yes | Wallet address |
| `limit` | query | `number` | no | Number of results to return (default: 20, max: 25) |
| `chains[]` | query | `array<string>` | no | Filter by blockchain(s) Send multiple values as a string separated by `,`. |
| `sort_by` | query | `string` | no | Sort field (default: usd_value) |
| `sort_direction` | query | `string` | no | Sort direction (default: desc) |
| `disable_spam_filtering` | query | `boolean` | no | Disable spam token filtering (default: false) |
| `cursor` | query | `string` | no | Pagination cursor for next page |
