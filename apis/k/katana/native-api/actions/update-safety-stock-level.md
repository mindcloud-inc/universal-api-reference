# Update Safety Stock Level with Katana

Updates an inventory safety stock level in Katana.

## Endpoint

- **Method:** `POST`
- **Path:** `/inventory_safety_stock_levels`
- **Base URL:** `https://api.katanamrp.com/v1`
- **Official documentation:** [Update Safety Stock Level](https://developer.katanamrp.com/reference/createinventorysafetystocklevel)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `location_id` | body | `number` | yes |
| `variant_id` | body | `number` | yes |
| `value` | body | `number` | yes |
