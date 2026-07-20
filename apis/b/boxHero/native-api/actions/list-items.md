# List Items with BoxHero

Retrieves items from BoxHero.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/items`
- **Base URL:** `https://rest.boxhero-app.com`
- **Official documentation:** [List Items](https://rest.boxhero-app.com/docs/api#/items/BarcodesController_getBarcodes)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cursor` | query | `number` | no | Cursor for the next page of items |
| `item_ids[]` | query | `array<number>` | no | Filter items by item ID |
| `limit` | query | `number` | no | Maximum number of items to return |
| `location_ids[]` | query | `array<number>` | no | Use these locations for quantity calculation |
