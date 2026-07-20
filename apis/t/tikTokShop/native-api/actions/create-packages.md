# Create Packages with TikTok Shop

## Endpoint

- **Method:** `POST`
- **Path:** `fulfillment/202309/packages`
- **Base URL:** `https://open-api.tiktokglobalshop.com/`
- **Official documentation:** [Create Packages](https://partner.tiktokshop.com/docv2/page/650aa132bace3e02b75d40d8?external_id=650aa132bace3e02b75d40d8#Back%20To%20Top)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `weight.unit` | body | `list` | no | Available values: - GRAM - POUND |
| `dimension.length` | body | `string` | no | — |
| `order_id` | body | `string` | yes | — |
| `weight.value` | body | `string` | no | — |
| `dimension.width` | body | `string` | no | — |
| `dimension.height` | body | `string` | no | — |
| `dimension.unit` | body | `list` | no | The unit of measurement for the package dimensions.  Available values: - CM - INCH |
| `shop_cipher` | query | `list<string>` | no | — |
| `dimension` | body | `object` | no | — |
| `order_line_item_ids` | body | `string` | no | — |
| `shipping_service_id` | body | `string` | no | — |
| `weight` | body | `object` | no | — |
