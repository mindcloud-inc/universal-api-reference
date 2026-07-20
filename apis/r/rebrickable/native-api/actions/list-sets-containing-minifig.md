# List Sets Containing Minifig with Rebrickable

Retrieves sets containing a LEGO minifig in Rebrickable.

## Endpoint

- **Method:** `GET`
- **Path:** `/lego/minifigs/:set_num/sets/`
- **Base URL:** `https://rebrickable.com/api/v3`
- **Official documentation:** [List Sets Containing Minifig](https://rebrickable.com/api/v3/docs/?key=xxxxxxxxxx)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `set_num` | path | `string` | yes | Rebrickable minifig set number. |
