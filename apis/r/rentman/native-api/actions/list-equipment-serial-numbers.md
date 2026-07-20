# List Equipment Serial Numbers with Rentman

## Endpoint

- **Method:** `GET`
- **Path:** `/equipment/:id/serialnumbers`
- **Base URL:** `https://api.rentman.net`
- **Official documentation:** [List Equipment Serial Numbers](https://api.rentman.net/#operation/getEquipmentSerialNumberCollection)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Numeric Rentman equipment identifier. |
