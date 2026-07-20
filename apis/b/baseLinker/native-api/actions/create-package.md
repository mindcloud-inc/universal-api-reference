# Create Package with BaseLinker

Creates a shipping package in BaseLinker.

## Endpoint

- **Method:** `POST`
- **Path:** `/connector.php`
- **Base URL:** `https://api.baselinker.com`
- **Official documentation:** [Create Package](https://api.baselinker.com/index.php?method=createPackage)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `order_id` | body | `number` | yes |
| `courier_code` | body | `string` | yes |
| `account_id` | body | `number` | no |
| `fields[]` | body | `array<object>` | no |
| `packages[]` | body | `array<object>` | no |
| `parameters` | body | `object` | no |
