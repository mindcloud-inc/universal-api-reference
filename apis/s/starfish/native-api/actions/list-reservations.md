# List Reservations with Starfish

Retrieves a list of reservations from Starfish.

## Endpoint

- **Method:** `GET`
- **Path:** `/reservations`
- **Base URL:** `https://api.camping.care/v21`
- **Official documentation:** [List Reservations](https://documenter.getpostman.com/view/9467805/VUjQkj1d)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of reservations to return. |
| `offset` | query | `number` | no | Number of reservations to skip before returning results. |
| `count` | query | `boolean` | no | Return the total reservation count instead of rows when true. |
| `order_by` | query | `string` | no | Sort reservations by id, last_modified, arrival, or departure. |
| `order` | query | `string` | no | Sort direction: asc or desc. |
| `status` | query | `string` | no | Filter reservations by status. |
| `arrival` | query | `date` | no | Filter reservations by arrival date or date range. |
| `departure` | query | `date` | no | Filter reservations by departure date or date range. |
| `accommodation_id` | query | `number` | no | Return only reservations for a specific accommodation. |
| `contact_id` | query | `number` | no | Return only reservations for a specific contact. |
