# Get Best Listing By NFT with OpenSea

Retrieves the best listing for an NFT in OpenSea.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/listings/collection/{slug}/nfts/{identifier}/best`
- **Base URL:** `https://api.opensea.io`
- **Official documentation:** [Get Best Listing By NFT](https://docs.opensea.io/reference/get_best_listing_nft)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `slug` | path | `string` | yes | Unique string to identify a collection on OpenSea |
| `identifier` | path | `string` | yes | NFT token id |
| `include_private_listings` | query | `boolean` | no | Whether to include private listings; defaults to false |
