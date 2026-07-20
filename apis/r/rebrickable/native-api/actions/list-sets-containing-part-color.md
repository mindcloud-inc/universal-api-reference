# List Sets Containing Part Color with Rebrickable

Retrieves sets containing a LEGO part color in Rebrickable.

## Endpoint

- **Method:** `GET`
- **Path:** `/lego/parts/:part_num/colors/:color_id/sets/`
- **Base URL:** `https://rebrickable.com/api/v3`
- **Official documentation:** [List Sets Containing Part Color](https://rebrickable.com/api/v3/docs/?key=xxxxxxxxxx)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `part_num` | path | `string` | yes | Rebrickable part number. |
| `color_id` | path | `number` | yes | Rebrickable color ID. |
