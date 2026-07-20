# Get Wallet Token Balances with Chainstream

Retrieves wallet token balances from Chainstream.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/wallet/:chain/:walletAddress/tokens-balance`
- **Base URL:** `https://api.chainstream.io`
- **Official documentation:** [Get Wallet Token Balances](https://docs.chainstream.io/en/api-reference/endpoint/data/wallet/v2/wallet-chain-walletaddress-tokens-balance-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chain` | path | `string` | yes | A chain name listed in supported networks. |
| `walletAddress` | path | `string` | yes | An address of a wallet. |
| `cursor` | query | `string` | no | Pagination cursor. |
| `limit` | query | `number` | no | Number of results per page. |
| `direction` | query | `string` | no | Pagination direction (next or prev). |
