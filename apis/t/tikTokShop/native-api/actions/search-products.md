# Search Products with TikTok Shop

## Endpoint

- **Method:** `POST`
- **Path:** `product/202502/products/search`
- **Base URL:** `https://open-api.tiktokglobalshop.com/`
- **Official documentation:** [Search Products](https://partner.tiktokshop.com/docv2/page/search-products-202502)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sku_ids[]` | body | `array<string>` | no | — |
| `seller_skus[]` | body | `array<string>` | no | — |
| `status` | body | `string` | no | Filter products by their status. Default: ALL Possible values:  - ALL - DRAFT - PENDING - FAILED - ACTIVATE - SELLER_DEACTIVATED - PLATFORM_DEACTIVATED - FREEZE - DELETED |
| `shop_cipher` | query | `list<string>` | yes | — |
| `sort_field` | query | `string` | no | — |
| `sort_order` | query | `string` | no | — |
