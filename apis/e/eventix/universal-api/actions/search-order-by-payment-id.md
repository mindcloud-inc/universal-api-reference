# Eventix: Get Order status link

Finds an Eventix order status link by payment ID.

```
GET https://connect.mindcloud.co/v1/universal/eventix/latest/actions/search-order-by-payment-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eventix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eventix/latest/actions/search-order-by-payment-id?connectionId=$CONNECTION_ID&paymentId=payment_123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "paymentId": "payment_123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eventix/latest/actions/search-order-by-payment-id?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `paymentId` | string | yes | The payment_id path parameter used to search for an order status link. Example: `payment_123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "download_link": "https://example.com",
      "order_id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `download_link` | string |  |
| `order_id` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Eventix API, this operation is `GET /3.0.0/order/search/:payment_id` (base URL `https://api.weeztix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-order-by-payment-id.md) for the provider-specific parameters and requirements.

