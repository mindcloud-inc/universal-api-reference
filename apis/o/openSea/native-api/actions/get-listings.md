# Get Listings with OpenSea

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/orders/{chain}/{protocol}/listings`
- **Base URL:** `https://api.opensea.io`
- **Official documentation:** [Get Listings](https://docs.opensea.io/reference/get_listings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chain` | path | `string` | yes | The blockchain on which to filter the results |
| `protocol` | path | `string` | yes | Protocol name (e.g. 'seaport') |
| `asset_contract_address` | query | `string` | no | — |
| `token_ids[]` | query | `array<string>` | no | Send multiple values as a string separated by `,`. |
| `token_ids[]` | query | `array<string>` | no | Send multiple values as a string separated by `,`. |
| `maker` | query | `string` | no | — |
| `listed_before` | query | `string` | no | — |
| `listed_after` | query | `string` | no | — |
| `order_direction` | query | `string` | no | — |
| `order_by` | query | `string` | no | — |
| `include_private_listings` | query | `boolean` | no | Whether to include private listings; defaults to false |
| `limit` | query | `number` | no | Number of items to return per page |
| `cursor.value` | query | `string` | no | — |
