# List Set Minifigs with Rebrickable

Retrieves minifigs for a LEGO set in Rebrickable.

## Endpoint

- **Method:** `GET`
- **Path:** `/lego/sets/:set_num/minifigs/`
- **Base URL:** `https://rebrickable.com/api/v3`
- **Official documentation:** [List Set Minifigs](https://rebrickable.com/api/v3/docs/?key=xxxxxxxxxx)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `set_num` | path | `string` | yes | Rebrickable set number. |
