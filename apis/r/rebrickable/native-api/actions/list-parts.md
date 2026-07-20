# List Parts with Rebrickable

Finds LEGO part records in Rebrickable.

## Endpoint

- **Method:** `GET`
- **Path:** `/lego/parts/`
- **Base URL:** `https://rebrickable.com/api/v3`
- **Official documentation:** [List Parts](https://rebrickable.com/api/v3/docs/?key=xxxxxxxxxx)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Search term for part name or number. |
| `part_num` | query | `string` | no | Filter by one exact Rebrickable part number. |
| `part_nums` | query | `string` | no | Comma-separated Rebrickable part numbers to fetch together. |
| `part_cat_id` | query | `number` | no | Only return parts in this Rebrickable part category. |
| `color_id` | query | `number` | no | Only return parts in this Rebrickable color. |
| `bricklink_id` | query | `string` | no | Filter by BrickLink part ID. |
| `brickowl_id` | query | `string` | no | Filter by BrickOwl part ID. |
| `lego_id` | query | `string` | no | Filter by LEGO element or design ID. |
| `ldraw_id` | query | `string` | no | Filter by LDraw part ID. |
