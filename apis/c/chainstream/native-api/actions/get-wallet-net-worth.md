# Get Wallet Net Worth with Chainstream

Retrieves wallet net worth from Chainstream.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/wallet/:chain/:walletAddress/net-worth`
- **Base URL:** `https://api.chainstream.io`
- **Official documentation:** [Get Wallet Net Worth](https://docs.chainstream.io/en/api-reference/endpoint/data/wallet/v2/wallet-chain-walletaddress-net-worth-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chain` | path | `string` | yes | A chain name listed in supported networks. |
| `walletAddress` | path | `string` | yes | An address of a wallet. |
| `cursor` | query | `string` | no | Pagination cursor. |
| `limit` | query | `number` | no | Number of results per page. |
| `direction` | query | `string` | no | Pagination direction (next or prev). |
