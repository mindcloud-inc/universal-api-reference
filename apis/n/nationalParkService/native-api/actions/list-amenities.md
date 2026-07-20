# List Amenities with National Park Service

Retrieves amenities from National Park Service.

## Endpoint

- **Method:** `GET`
- **Path:** `/amenities`
- **Base URL:** `https://developer.nps.gov/api/v1`
- **Official documentation:** [List Amenities](https://www.nps.gov/subjects/developer/api-documentation.htm)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | no | Amenity unique ID. |
| `q` | query | `string` | no | Search term. |
