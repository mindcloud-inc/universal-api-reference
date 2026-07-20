# Verify AU Address with Addressfinder

Verifies a full Australian address in Addressfinder.

## Endpoint

- **Method:** `GET`
- **Path:** `/au/address/v2/verification`
- **Base URL:** `https://api.addressfinder.io/api`
- **Official documentation:** [Verify AU Address](https://addressfinder.com/au/docs/api/au/au-address-verification-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | The address to be verified. |
| `gnaf` | query | `string` | no | Set to 1 to query the GNAF database. |
| `paf` | query | `string` | no | Set to 1 to query the PAF database. |
| `gps` | query | `string` | no | Set to 1 to return latitude and longitude when available. |
| `extended` | query | `string` | no | Set to 1 to return additional GNAF metadata. |
| `census` | query | `number` | no | Census year used for statistical area identifiers. |
| `state_codes` | query | `string` | no | Filter results by state or territory codes. |
| `domain` | query | `string` | no | Registered domain used for activity monitoring. |
| `post_box` | query | `string` | no | Set to 0 to exclude box-type addresses from verification results. |
| `ascii` | query | `string` | no | Set to 1 to normalize special characters to ASCII equivalents. |
| `format` | query | `string` | no | Response format. |
