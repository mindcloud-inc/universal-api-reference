# Get AU Address Metadata with Addressfinder

Retrieves metadata for an Australian address from Addressfinder.

## Endpoint

- **Method:** `GET`
- **Path:** `/au/address/metadata`
- **Base URL:** `https://api.addressfinder.io/api`
- **Official documentation:** [Get AU Address Metadata](https://addressfinder.com/au/docs/api/au/au-address-metadata-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | yes | Unique address identifier obtained from the AU Address Autocomplete API. |
| `source` | query | `string` | no | Address source dataset filter. |
| `gps` | query | `string` | no | Set to 1 to include latitude and longitude when available. |
| `census` | query | `number` | no | Census year used for statistical area identifiers. |
| `domain` | query | `string` | no | Registered domain used for activity monitoring. |
| `ascii` | query | `string` | no | Set to 1 to normalize special characters to ASCII equivalents. |
| `format` | query | `string` | no | Response format. |
