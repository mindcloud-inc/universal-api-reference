# Get All Offers By Collection with OpenSea

Retrieves all offers for an OpenSea collection.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/offers/collection/{slug}/all`
- **Base URL:** `https://api.opensea.io`
- **Official documentation:** [Get All Offers By Collection](https://docs.opensea.io/reference/list_offers_collection_all)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `slug` | path | `string` | yes | Unique string to identify a collection on OpenSea |
| `limit` | query | `number` | no | Number of items to return per page |
| `next.value` | query | `string` | no | — |
