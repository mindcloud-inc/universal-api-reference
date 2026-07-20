# Autocomplete Order Address with Snappy

Finds shipping address suggestions in Snappy by partial input.

## Endpoint

- **Method:** `GET`
- **Path:** `/orders/addresses/autocomplete`
- **Base URL:** `https://api.snappy.com/public-api/v2`
- **Official documentation:** [Autocomplete Order Address](https://docs.snappy.com/reference/autocompleteorderaddress)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `address` | query | `string` | yes |
| `companyId` | query | `string` | yes |
| `country` | query | `string` | yes |
