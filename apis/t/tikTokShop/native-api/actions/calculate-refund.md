# Calculate Refund with TikTok Shop

## Endpoint

- **Method:** `POST`
- **Path:** `/return_refund/202602/refunds/calculate`
- **Base URL:** `https://open-api.tiktokglobalshop.com/`
- **Official documentation:** [Calculate Refund](https://partner.tiktokshop.com/docv2/page/calculate-refund-202602)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shop_cipher` | query | `string` | yes | — |
| `order_id` | body | `string` | yes | — |
| `request_type` | body | `list<string>` | yes | Accepted values: `CANCEL`, `REFUND`, `RETURN_AND_REFUND`. |
| `reason_name` | body | `string` | yes | Use a reason name returned by Get Aftersale Eligibility for the selected order. |
| `shipment_type` | body | `list<string>` | no | Accepted values: `BUYER_ARRANGE`, `PLATFORM`. |
| `handover_method` | body | `list<string>` | no | Accepted values: `DROP_OFF`, `PICKUP`. |
| `order_line_item_ids[]` | body | `array<string>` | no | Choose either these IDs or Order Line List. Omit all item selectors to estimate the entire order. |
| `skus[]` | body | `array<object>` | no | — |
| `skus[].sku_id` | body | `string` | yes | — |
| `skus[].quantity` | body | `number` | yes | — |
| `order_line_list[]` | body | `array<object>` | no | — |
| `order_line_list[].order_line_item_id` | body | `string` | no | — |
| `order_line_list[].sub_order_line_item_id` | body | `string` | no | Required for an item within a bundle; optional for other products. |
