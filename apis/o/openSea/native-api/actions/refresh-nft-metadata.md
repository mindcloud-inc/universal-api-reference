# Refresh NFT Metadata with OpenSea

Refreshes NFT metadata in OpenSea.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/chain/{chain}/contract/{address}/nfts/{identifier}/refresh`
- **Base URL:** `https://api.opensea.io`
- **Official documentation:** [Refresh NFT Metadata](https://docs.opensea.io/reference/refresh_nft_metadata)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | path | `string` | yes | Contract address |
| `chain` | path | `string` | yes | The blockchain on which to filter the results |
| `identifier` | path | `string` | yes | Token identifier |
| `ignoreCachedItemUrls` | query | `boolean` | no | — |
