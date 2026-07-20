# Create Purchase Order with Katana

Creates a new purchase order in Katana.

## Endpoint

- **Method:** `POST`
- **Path:** `/purchase_orders`
- **Base URL:** `https://api.katanamrp.com/v1`
- **Official documentation:** [Create Purchase Order](https://developer.katanamrp.com/reference/createpurchaseorder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `order_no` | body | `string` | yes | — |
| `entity_type` | body | `string` | no | — |
| `supplier_id` | body | `number` | yes | — |
| `currency` | body | `string` | no | E.g. USD, EUR. All currently active currency codes in ISO 4217 format. |
| `status` | body | `string` | no | — |
| `expected_arrival_date` | body | `string` | no | — |
| `order_created_date` | body | `string` | no | — |
| `location_id` | body | `number` | yes | — |
| `tracking_location_id` | body | `number` | no | Submittable only when entity_type is outsourced |
| `additional_info` | body | `string` | no | — |
| `purchase_order_rows[]` | body | `array<object>` | yes | — |
| `purchase_order_rows[].quantity` | body | `number` | yes | — |
| `purchase_order_rows[].variant_id` | body | `number` | yes | — |
| `purchase_order_rows[].tax_rate_id` | body | `number` | no | — |
| `purchase_order_rows[].price_per_unit` | body | `number` | yes | — |
| `purchase_order_rows[].purchase_uom_conversion_rate` | body | `number` | no | — |
| `purchase_order_rows[].purchase_uom` | body | `string` | no | Maximum length: 7. |
| `purchase_order_rows[].arrival_date` | body | `string` | no | — |
