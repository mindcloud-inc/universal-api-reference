# List Transactions by Order with TikTok Shop

## Endpoint

- **Method:** `GET`
- **Path:** `/finance/202501/orders/:order_id/statement_transactions`
- **Base URL:** `https://open-api.tiktokglobalshop.com/`
- **Official documentation:** [List Transactions by Order](https://partner.tiktokshop.com/docv2/page/get-transactions-by-order-202501)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `order_id` | path | `string` | yes |
| `shop_cipher` | query | `list<string>` | yes |
