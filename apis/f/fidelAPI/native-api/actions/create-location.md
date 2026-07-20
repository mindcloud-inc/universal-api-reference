# Create Location with Fidel API

Creates a location in a Fidel program.

## Endpoint

- **Method:** `POST`
- **Path:** `/programs/:programId/locations`
- **Base URL:** `https://api.fidel.uk/v1`
- **Official documentation:** [Create Location](https://reference.fidel.uk/reference/create-location)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `programId` | path | `string` | yes | — |
| `address` | body | `string` | yes | 2 - 100 characters. |
| `brandId` | body | `string` | yes | Brand identifier for the location. |
| `city` | body | `string` | yes | 2 - 100 characters. |
| `countryCode` | body | `string` | yes | Allowed values: CAN, DNK, FIN, GBR, IRL, JPN, NOR, SWE, USA. |
| `postcode` | body | `string` | yes | 4 - 20 characters. |
