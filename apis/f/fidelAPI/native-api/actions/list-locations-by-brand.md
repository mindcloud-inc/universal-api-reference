# List Locations by Brand with Fidel API

Retrieves locations for a brand in Fidel API.

## Endpoint

- **Method:** `GET`
- **Path:** `/brands/:brandId/programs/:programId/locations`
- **Base URL:** `https://api.fidel.uk/v1`
- **Official documentation:** [List Locations by Brand](https://reference.fidel.uk/reference/list-locations-by-brand)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `brandId` | path | `string` | yes | — |
| `programId` | path | `string` | yes | Program ID to search on. |
