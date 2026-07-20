# Get Best Listings By Collection with OpenSea

Retrieves best listings for an OpenSea collection.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/listings/collection/{slug}/best`
- **Base URL:** `https://api.opensea.io`
- **Official documentation:** [Get Best Listings By Collection](https://docs.opensea.io/reference/get_best_listings_collection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `slug` | path | `string` | yes | Unique string to identify a collection on OpenSea |
| `include_private_listings` | query | `boolean` | no | Whether to include private listings; defaults to false |
| `limit` | query | `number` | no | Number of items to return per page |
| `next.value` | query | `string` | no | — |
