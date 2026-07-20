# Get All Listings By Collection with OpenSea

Retrieves all listings for an OpenSea collection.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/listings/collection/{slug}/all`
- **Base URL:** `https://api.opensea.io`
- **Official documentation:** [Get All Listings By Collection](https://docs.opensea.io/reference/list_listings_collection_all)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `slug` | path | `string` | yes | Unique string to identify a collection on OpenSea |
| `include_private_listings` | query | `boolean` | no | Whether to include private listings; defaults to false |
| `limit` | query | `number` | no | Number of items to return per page |
| `next.value` | query | `string` | no | — |
