# Cancel Order with TikTok Shop

Use this API to cancel an order on behalf of a seller. In the US and UK markets, when an item is out of stock, partial cancellation on the single item level is supported by this API.

## Endpoint

- **Method:** `POST`
- **Path:** `return_refund/202309/cancellations`
- **Base URL:** `https://open-api.tiktokglobalshop.com/`
- **Official documentation:** [Cancel Order](https://partner.tiktokshop.com/docv2/page/cancel-order-202309)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shopCipher` | query | `list<string>` | no | — |
| `skus.skuId` | body | `string` | yes | — |
| `orderId` | body | `string` | yes | TikTok Shop order id |
| `skus.quantity` | body | `number` | yes | — |
| `skus` | body | `object` | no | — |
| `orderLineitemids[]` | body | `array` | no | List of order line item ids to cancel. In the US and UK markets, when an item is out of stock, partial cancellation on the single item level is supported. To initiate a partial cancellation, specify the item's order line id. |
| `cancelReason` | body | `string` | yes | Reason to cancel the order  UNPAID Out of stock seller_cancel_unpaid_reason_out_of_stock Pricing error seller_cancel_unpaid_reason_wrong_price Buyer did not pay on time seller_cancel_unpaid_reason_buyer_hasnt_paid_within_time_allowed Buyer requested cancellation seller_cancel_unpaid_reason_buyer_requested_cancellation ON_HOLD and AWAITING_SHIPMENT Out of stock seller_cancel_reason_out_of_stock Pricing error seller_cancel_reason_wrong_price Unable to deliver to buyer address seller_cancel_paid_reason_address_not_deliver Buyer requested cancellation seller_cancel_paid_reason_buyer_requested_cancellation |
