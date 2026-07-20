# Update Inventory with TikTok Shop

## Endpoint

- **Method:** `POST`
- **Path:** `product/202309/products/:product_id/inventory/update`
- **Base URL:** `https://open-api.tiktokglobalshop.com/`
- **Official documentation:** [Update Inventory](https://partner.tiktokshop.com/doc/page/63fd742b715d622a338c4bbf?external_id=63fd742b715d622a338c4bbf)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `product_id` | path | `string` | yes |
| `skus[].id` | body | `string` | no |
| `skus[].inventory[].warehouse_id` | body | `string` | no |
| `skus[].inventory[]` | body | `array` | no |
| `skus[].inventory[].quantity` | body | `number` | no |
| `shop_cipher` | query | `list<string>` | no |
| `skus[]` | body | `array` | no |
