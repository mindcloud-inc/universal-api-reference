# Get Offers By NFT with OpenSea

Retrieves offers for an NFT in OpenSea.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/offers/collection/{slug}/nfts/{identifier}`
- **Base URL:** `https://api.opensea.io`
- **Official documentation:** [Get Offers By NFT](https://docs.opensea.io/reference/get_offers_nft)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `slug` | path | `string` | yes | Unique string to identify a collection on OpenSea |
| `identifier` | path | `string` | yes | NFT token id |
| `limit` | query | `number` | no | Number of items to return per page |
| `next.value` | query | `string` | no | — |
