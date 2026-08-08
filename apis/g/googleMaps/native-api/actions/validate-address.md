# Validate Address with Google Maps

Validates an Address

## Endpoint

- **Method:** `POST`
- **Path:** `https://addressvalidation.googleapis.com/v1::validateAddress?alt=json&fields=*`
- **Official documentation:** [Validate Address](https://developers.google.com/maps/documentation/address-validation/reference/rest/v1/TopLevel/validateAddress)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | body | `object` | no | — |
| `address.regionCode` | body | `string` | no | Optional, but helpful for a complete validation. i.e. `CA` for Canada. |
| `address.addressLines` | body | `string` | no | Required. Unstructured address lines describing the lower levels of an address.  Because values in addressLines do not have type information and may sometimes contain multiple values in a single field (e.g. "Austin, TX"), it is important that the line order is clear. The order of address lines should be "envelope order" for the country/region of the address.  The minimum permitted structural representation of an address consists of all information placed in the addressLines. If a regionCode is not provided, the region is inferred from the address lines.  Creating an address only containing addressLines, and then geocoding is the recommended way to handle completely unstructured addresses (as opposed to guessing which parts of the address should be localities or administrative areas). Send multiple values as a array. |
