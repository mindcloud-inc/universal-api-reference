# Set Order Product Fields with BaseLinker

Updates order product fields in BaseLinker.

## Endpoint

- **Method:** `POST`
- **Path:** `/connector.php`
- **Base URL:** `https://api.baselinker.com`
- **Official documentation:** [Set Order Product Fields](https://api.baselinker.com/index.php?method=setOrderProductFields)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `order_id` | body | `number` | yes | Order identifier. |
| `order_product_id` | body | `number` | yes | Order product line identifier to update. |
| `name` | body | `string` | no | Updated product name. |
| `sku` | body | `string` | no | Updated SKU value. |
| `ean` | body | `string` | no | Updated EAN value. |
| `price_brutto` | body | `number` | no | Updated gross item price. |
| `quantity` | body | `number` | no | Updated quantity value. |
| `tax_rate` | body | `number` | no | Updated VAT rate percentage. |
| `attributes` | body | `object` | no | Updated product attributes payload. |
| `parameters` | body | `object` | no | Optional raw BaseLinker parameters merged with the typed fields before request serialization. |
