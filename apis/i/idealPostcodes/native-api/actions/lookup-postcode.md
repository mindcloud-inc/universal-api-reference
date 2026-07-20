# Lookup Postcode with Ideal Postcodes

Retrieves addresses from Ideal Postcodes for a UK postcode.

## Endpoint

- **Method:** `GET`
- **Path:** `/postcodes/:postcode`
- **Base URL:** `https://api.ideal-postcodes.co.uk/v1`
- **Official documentation:** [Lookup Postcode](https://docs.ideal-postcodes.co.uk/docs/api/postcodes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `postcode` | path | `string` | yes | UK postcode to look up. |
| `filter` | query | `string` | no | Comma-separated whitelist of address fields to return. |
| `page` | query | `number` | no | Zero-indexed page of results to return. |
| `tags` | query | `string` | no | Comma-separated tags to associate with the lookup. |
