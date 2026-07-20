# Get NFTs By Account with OpenSea

Retrieves NFTs owned by an OpenSea account.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/chain/{chain}/account/{address}/nfts`
- **Base URL:** `https://api.opensea.io`
- **Official documentation:** [Get NFTs By Account](https://docs.opensea.io/reference/get_nfts_by_account)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | path | `string` | yes | Account address |
| `chain` | path | `string` | yes | The blockchain on which to filter the results |
| `collection` | query | `string` | no | — |
| `limit` | query | `number` | no | Number of items to return per page |
| `next.value` | query | `string` | no | — |
