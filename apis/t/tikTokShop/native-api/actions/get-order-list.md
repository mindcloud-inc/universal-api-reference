# Get Order List with TikTok Shop

## Endpoint

- **Method:** `POST`
- **Path:** `order/202309/orders/search`
- **Base URL:** `https://open-api.tiktokglobalshop.com/`
- **Official documentation:** [Get Order List](https://partner.tiktokshop.com/docv2/page/650aa8094a0bb702c06df242?external_id=650aa8094a0bb702c06df242)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `buyer_user_id` | body | `string` | no | — |
| `create_time_ge` | body | `date` | no | — |
| `create_time_lt` | body | `date` | no | — |
| `is_buyer_request_cancel` | body | `boolean` | no | Format: `toggle`. |
| `order_status` | body | `list<string>` | no | — |
| `shipping_type` | body | `list<string>` | no | — |
| `shop_cipher` | query | `list<string>` | yes | — |
| `sort_field` | query | `string` | no | — |
| `sort_order` | query | `string` | no | — |
| `update_time_ge` | body | `date` | no | — |
| `update_time_lt` | body | `date` | no | — |
| `warehouse_ids` | body | `string` | no | Send multiple values as a array. |
