# List NFTs from Wallet with Crossmint

Retrieves NFTs from a Crossmint wallet.

## Endpoint

- **Method:** `GET`
- **Path:** `/2022-06-09/wallets/:identifier/nfts`
- **Base URL:** `https://staging.crossmint.com/api`
- **Official documentation:** [List NFTs from Wallet](https://docs.crossmint.com/api-reference/wallets/get-nfts-from-wallet)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | Wallet identifier or address for the wallet NFT query. |
| `page` | query | `string` | no | Page index. |
| `perPage` | query | `string` | no | Number of items per page. |
