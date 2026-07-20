# Get NFTs By Collection with OpenSea

Retrieves NFTs in an OpenSea collection.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/collection/{slug}/nfts`
- **Base URL:** `https://api.opensea.io`
- **Official documentation:** [Get NFTs By Collection](https://docs.opensea.io/reference/get_nfts_by_collection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `slug` | path | `string` | yes | Collection slug |
| `limit` | query | `number` | no | Number of items to return per page |
| `next.value` | query | `string` | no | — |
