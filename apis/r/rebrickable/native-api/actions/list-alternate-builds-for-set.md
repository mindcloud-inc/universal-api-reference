# List Alternate Builds for Set with Rebrickable

Retrieves alternate builds for a LEGO set in Rebrickable.

## Endpoint

- **Method:** `GET`
- **Path:** `/lego/sets/:set_num/alternates/`
- **Base URL:** `https://rebrickable.com/api/v3`
- **Official documentation:** [List Alternate Builds for Set](https://rebrickable.com/api/v3/docs/?key=xxxxxxxxxx)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `set_num` | path | `string` | yes | Rebrickable set number. |
