# Batch Update Inventory Levels with Loyverse

Updates inventory levels in batch in Loyverse.

## Endpoint

- **Method:** `POST`
- **Path:** `/inventory`
- **Base URL:** `https://api.loyverse.com/v1.0`
- **Official documentation:** [Batch Update Inventory Levels](https://developer.loyverse.com/docs/#tag/Inventory)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `inventory_levels[]` | body | `array<object>` | no |
