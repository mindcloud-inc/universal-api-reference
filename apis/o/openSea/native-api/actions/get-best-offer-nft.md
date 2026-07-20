# Get Best Offer By NFT with OpenSea

Retrieves the best offer for an NFT in OpenSea.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/offers/collection/{slug}/nfts/{identifier}/best`
- **Base URL:** `https://api.opensea.io`
- **Official documentation:** [Get Best Offer By NFT](https://docs.opensea.io/reference/get_best_offer_nft)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `slug` | path | `string` | yes | Unique string to identify a collection on OpenSea |
| `identifier` | path | `string` | yes | NFT token id |
