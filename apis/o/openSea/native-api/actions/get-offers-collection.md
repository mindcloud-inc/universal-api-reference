# Get Offers By Collection with OpenSea

Retrieves offers for an OpenSea collection.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/offers/collection/{slug}`
- **Base URL:** `https://api.opensea.io`
- **Official documentation:** [Get Offers By Collection](https://docs.opensea.io/reference/get_offers_collection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `slug` | path | `string` | yes | Unique string to identify a collection on OpenSea |
| `limit` | query | `number` | no | Number of items to return per page |
| `next.value` | query | `string` | no | — |
