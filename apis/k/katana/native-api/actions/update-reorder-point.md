# Update Reorder Point with Katana

Updates an inventory reorder point in Katana.

## Endpoint

- **Method:** `POST`
- **Path:** `/inventory_reorder_points`
- **Base URL:** `https://api.katanamrp.com/v1`
- **Official documentation:** [Update Reorder Point](https://developer.katanamrp.com/reference/update-reorder-point)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `location_id` | body | `number` | yes |
| `variant_id` | body | `number` | yes |
| `value` | body | `number` | yes |
