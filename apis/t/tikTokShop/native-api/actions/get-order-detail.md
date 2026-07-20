# Get Order Detail with TikTok Shop

## Endpoint

- **Method:** `GET`
- **Path:** `order/202309/orders`
- **Base URL:** `https://open-api.tiktokglobalshop.com/`
- **Official documentation:** [Get Order Detail](https://partner.tiktokshop.com/docv2/page/6507ead7b99d5302be949ba9?external_id=6507ead7b99d5302be949ba9)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids` | query | `string<string>` | no | A list of TikTok Shop order ID values. **max: 50 per request** Maximum length: 50. Send multiple values as a array. |
| `shop_cipher` | query | `list<list>` | no | — |
