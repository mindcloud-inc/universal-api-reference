# List Minifigs with Rebrickable

Finds LEGO minifig records in Rebrickable.

## Endpoint

- **Method:** `GET`
- **Path:** `/lego/minifigs/`
- **Base URL:** `https://rebrickable.com/api/v3`
- **Official documentation:** [List Minifigs](https://rebrickable.com/api/v3/docs/?key=xxxxxxxxxx)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Search term for minifig name or number. |
| `min_parts` | query | `number` | no | Only return minifigs with at least this many parts. |
| `max_parts` | query | `number` | no | Only return minifigs with at most this many parts. |
| `in_set_num` | query | `string` | no | Only return minifigs that appear in this set number. |
| `in_theme_id` | query | `number` | no | Only return minifigs that appear in this theme ID. |
