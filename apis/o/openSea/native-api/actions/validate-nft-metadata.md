# Validate NFT Metadata with OpenSea

Validates NFT metadata in OpenSea.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/chain/{chain}/contract/{address}/nfts/{identifier}/validate-metadata`
- **Base URL:** `https://api.opensea.io`
- **Official documentation:** [Validate NFT Metadata](https://docs.opensea.io/reference/validate_nft_metadata)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chain` | path | `string` | yes | The blockchain on which to filter the results |
| `address` | path | `string` | yes | The contract address |
| `identifier` | path | `string` | yes | The NFT token id |
| `ignoreCachedItemUrls` | query | `boolean` | no | Whether to bypass cached SeaDN URLs |
