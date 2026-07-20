# List Locations with Fidel API

Retrieves locations from a Fidel program.

## Endpoint

- **Method:** `GET`
- **Path:** `/programs/:programId/locations`
- **Base URL:** `https://api.fidel.uk/v1`
- **Official documentation:** [List Locations](https://reference.fidel.uk/reference/list-locations)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `programId` | path | `string` | yes |
