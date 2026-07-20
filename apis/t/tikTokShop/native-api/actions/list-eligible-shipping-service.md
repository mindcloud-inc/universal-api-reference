# List Eligible Shipping Service with TikTok Shop

Use this API ( for US ) to query the list of available shipping services when specifying packages' size or weight. The shipping fee and delivery time is an estimate only and is based on the package dimensions and weight you provided. Options listed may differ if you change the package attributes at the time of shipping.

## Endpoint

- **Method:** `POST`
- **Path:** `/fulfillment/202309/orders/:orderId/shipping_services/query`
- **Base URL:** `https://open-api.tiktokglobalshop.com/`
- **Official documentation:** [List Eligible Shipping Service](https://partner.tiktokshop.com/docv2/page/650aa6b2bace3e02b75dda4e?external_id=650aa6b2bace3e02b75dda4e)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dimension.length` | body | `string` | no | — |
| `orderId` | path | `string` | no | — |
| `weight.value` | body | `string` | no | — |
| `dimension.height` | body | `string` | no | — |
| `shop_cipher` | query | `list` | no | — |
| `weight.unit` | body | `list` | no | The unit of measurement is used to measure the weight. - GRAM - POUND |
| `dimension.width` | body | `string` | no | — |
| `order_line_item_ids` | body | `string` | no | — |
| `dimension.unit` | body | `list` | no | The unit of measurement is used to measure the length. - CM - INCH |
| `dimension` | body | `object` | no | — |
| `weight` | body | `object` | no | — |
