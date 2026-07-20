# List AU Address Suggestions with Addressfinder

Finds Australian address suggestions in Addressfinder by partial query.

## Endpoint

- **Method:** `GET`
- **Path:** `/au/address/autocomplete`
- **Base URL:** `https://api.addressfinder.io/api`
- **Official documentation:** [List AU Address Suggestions](https://addressfinder.com/au/docs/api/au/au-address-autocomplete-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | no | The partial address being searched. |
| `source` | query | `string` | no | Address source dataset filter. |
| `state_codes` | query | `string` | no | Filter results by state or territory codes. |
| `max` | query | `number` | no | Maximum number of suggestions to return. |
| `format` | query | `string` | no | Response format. |
| `domain` | query | `string` | no | Registered domain used for activity monitoring. |
| `post_box` | query | `string` | no | Include or restrict PO Box style addresses. |
| `canonical` | query | `string` | no | Exclude alias addresses when set. |
| `highlight` | query | `string` | no | Highlight matching terms in the returned address text. |
| `ascii` | query | `string` | no | Normalize special characters to ASCII equivalents. |
