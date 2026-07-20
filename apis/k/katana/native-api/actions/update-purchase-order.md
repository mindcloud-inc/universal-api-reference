# Update Purchase Order with Katana

Updates an existing purchase order in Katana.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/purchase_orders/:id`
- **Base URL:** `https://api.katanamrp.com/v1`
- **Official documentation:** [Update Purchase Order](https://developer.katanamrp.com/reference/updatepurchaseorder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Purchase order id |
| `order_no` | body | `string` | no | Updatable only when status is in DRAFT, NOT_RECEIVED and PARTIALLY_RECEIVED |
| `supplier_id` | body | `number` | no | Updatable only when status is in DRAFT and NOT_RECEIVED |
| `currency` | body | `string` | no | Updatable only when status is in DRAFT and NOT_RECEIVED |
| `tracking_location_id` | body | `string` | no | Updatable only when status is in DRAFT and NOT_RECEIVED and         entity_type is outsourced |
| `status` | body | `string` | no | — |
| `expected_arrival_date` | body | `string` | no | Updatable only when status is in DRAFT, NOT_RECEIVED and PARTIALLY_RECEIVED. Update will override arrival_date on purchase order rows |
| `order_created_date` | body | `string` | no | — |
| `location_id` | body | `number` | no | Updatable only when status is in DRAFT and NOT_RECEIVED |
| `additional_info` | body | `string` | no | — |
