# List Minifig Parts with Rebrickable

Retrieves parts for a LEGO minifig in Rebrickable.

## Endpoint

- **Method:** `GET`
- **Path:** `/lego/minifigs/:set_num/parts/`
- **Base URL:** `https://rebrickable.com/api/v3`
- **Official documentation:** [List Minifig Parts](https://rebrickable.com/api/v3/docs/?key=xxxxxxxxxx)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `set_num` | path | `string` | yes | Rebrickable minifig set number. |
