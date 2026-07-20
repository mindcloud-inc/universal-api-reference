# Update Location with Fidel API

Updates an existing location in Fidel API.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/locations/:locationId`
- **Base URL:** `https://api.fidel.uk/v1`
- **Official documentation:** [Update Location](https://reference.fidel.uk/reference/update-location)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `locationId` | path | `string` | yes | — |
| `address` | body | `string` | yes | Address for the location. |
| `city` | body | `string` | yes | City for the location. |
| `countryCode` | body | `string` | yes | ISO alpha-3 country code for the location. |
| `postcode` | body | `string` | yes | Postcode for the location. |
