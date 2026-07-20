# Get Wallet Net Worth Details with Chainstream

Retrieves wallet net worth details from Chainstream.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/wallet/:chain/:walletAddress/net-worth-details`
- **Base URL:** `https://api.chainstream.io`
- **Official documentation:** [Get Wallet Net Worth Details](https://docs.chainstream.io/en/api-reference/endpoint/data/wallet/v2/wallet-chain-walletaddress-net-worth-details-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chain` | path | `string` | yes | A chain name listed in supported networks. |
| `walletAddress` | path | `string` | yes | An address of a wallet. |
| `cursor` | query | `string` | no | Pagination cursor. |
| `limit` | query | `number` | no | Number of results per page. |
| `direction` | query | `string` | no | Pagination direction (next or prev). |
| `hours` | query | `number` | no | Historical snapshot hours (0 for realtime). |
