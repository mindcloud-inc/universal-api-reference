# Get Offers By Trait with OpenSea

Retrieves offers for a trait in OpenSea.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/offers/collection/{slug}/traits`
- **Base URL:** `https://api.opensea.io`
- **Official documentation:** [Get Offers By Trait](https://docs.opensea.io/reference/get_offers_collection_trait)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `slug` | path | `string` | yes | Unique string to identify a collection on OpenSea |
| `type` | query | `string` | no | Trait type (deprecated: use 'traits' parameter) |
| `value` | query | `string` | no | Trait value as string (deprecated: use 'traits' parameter) |
| `float_value` | query | `number` | no | Trait value as float (deprecated: use 'traits' parameter) |
| `int_value` | query | `number` | no | Trait value as integer (deprecated: use 'traits' parameter) |
| `traits` | query | `string` | no | JSON array of trait filters. Each trait has 'traitType' and 'value' fields. Example: [{"traitType":"Background","value":"Red"},{"traitType":"Eyes","value":"Blue"}] |
| `limit` | query | `number` | no | Number of items to return per page |
| `next.value` | query | `string` | no | — |
