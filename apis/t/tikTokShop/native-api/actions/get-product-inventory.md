# Get Product Inventory with TikTok Shop

Use this api to get product stock details.

## Endpoint

- **Method:** `POST`
- **Path:** `product/202309/inventory/search`
- **Base URL:** `https://open-api.tiktokglobalshop.com/`
- **Official documentation:** [Get Product Inventory](https://partner.tiktokshop.com/doc/page/649a5faa600c3a0288889b35?external_id=649a5faa600c3a0288889b35#Back%20To%20Top)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shop_cipher` | query | `list<string>` | no | — |
| `product_ids` | body | `string` | no | Send multiple values as a array. |
| `sku_ids` | body | `string` | no | Send multiple values as a array. |
