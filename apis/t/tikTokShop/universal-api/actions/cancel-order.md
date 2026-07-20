# TikTok Shop: Cancel Order

Use this API to cancel an order on behalf of a seller. In the US and UK markets, when an item is out of stock, partial cancellation on the single item level is supported by this API.

```
PUT https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/cancel-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TikTok Shop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/cancel-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "skus.skuId": "string",
  "orderId": "string",
  "skus.quantity": 1,
  "cancelReason": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/cancel-order', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "skus.skuId": "string",
    "orderId": "string",
    "skus.quantity": 1,
    "cancelReason": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `shopCipher` | list<string> | no |  |
| `skus.skuId` | string | yes |  |
| `orderId` | string | yes | TikTok Shop order id |
| `skus.quantity` | number | yes |  |
| `skus` | object | no |  |
| `orderLineitemids[]` | array | no | List of order line item ids to cancel. In the US and UK markets, when an item is out of stock, partial cancellation on the single item level is supported. To initiate a partial cancellation, specify the item's order line id. |
| `cancelReason` | string | yes | Reason to cancel the order UNPAID Out of stock seller_cancel_unpaid_reason_out_of_stock Pricing error seller_cancel_unpaid_reason_wrong_price Buyer did not pay on time seller_cancel_unpaid_reason_buyer_hasnt_paid_within_time_allowed Buyer requested cancellation seller_cancel_unpaid_reason_buyer_requested_cancellation ON_HOLD and AWAITING_SHIPMENT Out of stock seller_cancel_reason_out_of_stock Pricing error seller_cancel_reason_wrong_price Unable to deliver to buyer address seller_cancel_paid_reason_address_not_deliver Buyer requested cancellation seller_cancel_paid_reason_buyer_requested_cancellation |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native TikTok Shop API returns.

## Native endpoint

Through the native TikTok Shop API, this operation is `POST return_refund/202309/cancellations` (base URL `https://open-api.tiktokglobalshop.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-order.md) for the provider-specific parameters and requirements.

