# Get Item Offers with OpenSea

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/orders/{chain}/{protocol}/offers`
- **Base URL:** `https://api.opensea.io`
- **Official documentation:** [Get Item Offers](https://docs.opensea.io/reference/get_offers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chain` | path | `string` | no | The blockchain on which to filter the results |
| `chain` | path | `string` | yes | The blockchain on which to filter the results |
| `protocol` | path | `string` | yes | Protocol name (e.g. 'seaport') |
| `asset_contract_address` | query | `string` | no | — |
| `token_ids[]` | query | `array<string>` | no | Send multiple values as a string separated by `,`. |
| `token_ids[]` | query | `array<string>` | no | Send multiple values as a string separated by `,`. |
| `maker` | query | `string` | no | — |
| `order_direction` | query | `string` | no | — |
| `order_by` | query | `string` | no | — |
| `listed_before` | query | `string` | no | — |
| `listed_after` | query | `string` | no | — |
| `payment_token_address` | query | `string` | no | — |
| `limit` | query | `number` | no | Number of items to return per page |
| `cursor.value` | query | `string` | no | — |
