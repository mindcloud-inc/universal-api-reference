# Create Sales Order Fulfillment with Katana

Creates a sales order fulfillment in Katana.

## Endpoint

- **Method:** `POST`
- **Path:** `/sales_order_fulfillments`
- **Base URL:** `https://api.katanamrp.com/v1`
- **Official documentation:** [Create Sales Order Fulfillment](https://developer.katanamrp.com/reference/create-sales-order-fulfillment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sales_order_id` | body | `number` | yes | — |
| `picked_date` | body | `string` | no | — |
| `status` | body | `string` | yes | — |
| `conversion_rate` | body | `number` | no | — |
| `conversion_date` | body | `string` | no | — |
| `tracking_number` | body | `string` | no | Maximum length: 256. |
| `tracking_url` | body | `string` | no | Maximum length: 2048. |
| `tracking_carrier` | body | `string` | no | — |
| `tracking_method` | body | `string` | no | — |
| `sales_order_fulfillment_rows[]` | body | `array<object>` | no | — |
| `sales_order_fulfillment_rows[].sales_order_row_id` | body | `number` | no | — |
| `sales_order_fulfillment_rows[].quantity` | body | `number` | no | — |
| `sales_order_fulfillment_rows[].batch_transactions[]` | body | `array<object>` | no | — |
| `sales_order_fulfillment_rows[].batch_transactions[].batch_id` | body | `number` | no | — |
| `sales_order_fulfillment_rows[].batch_transactions[].quantity` | body | `number` | no | — |
| `sales_order_fulfillment_rows[].serial_numbers[]` | body | `array<number>` | no | — |
