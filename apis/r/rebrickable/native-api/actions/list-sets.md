# List Sets with Rebrickable

Finds LEGO set records in Rebrickable.

## Endpoint

- **Method:** `GET`
- **Path:** `/lego/sets/`
- **Base URL:** `https://rebrickable.com/api/v3`
- **Official documentation:** [List Sets](https://rebrickable.com/api/v3/docs/?key=xxxxxxxxxx)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Search term for set name or set number. |
| `theme_id` | query | `number` | no | Only return sets in this Rebrickable theme ID. |
| `min_year` | query | `number` | no | Only return sets released in or after this year. |
| `max_year` | query | `number` | no | Only return sets released in or before this year. |
| `min_parts` | query | `number` | no | Only return sets with at least this many parts. |
| `max_parts` | query | `number` | no | Only return sets with at most this many parts. |
