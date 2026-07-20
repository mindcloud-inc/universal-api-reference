# List Part Colors with Rebrickable

Retrieves available colors for a LEGO part in Rebrickable.

## Endpoint

- **Method:** `GET`
- **Path:** `/lego/parts/:part_num/colors/`
- **Base URL:** `https://rebrickable.com/api/v3`
- **Official documentation:** [List Part Colors](https://rebrickable.com/api/v3/docs/?key=xxxxxxxxxx)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `part_num` | path | `string` | yes | Rebrickable part number. |
