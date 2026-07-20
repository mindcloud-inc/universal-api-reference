# CoinGate: Get Order Refund

Retrieves a refund for a specific CoinGate order.

```
GET https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/get-order-refund
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoinGate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/get-order-refund?connectionId=$CONNECTION_ID&orderId=1&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orderId": "1",
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/get-order-refund?${params}`, {
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
| `orderId` | number | yes | CoinGate order ID. |
| `id` | number | yes | CoinGate refund ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "id": 1,
      "refundAmount": "string",
      "requestAmount": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `id` | number |  |
| `refundAmount` | string |  |
| `requestAmount` | string |  |
| `status` | string |  |

## Native endpoint

Through the native CoinGate API, this operation is `GET /orders/:order_id/refunds/:id` (base URL `https://api.coingate.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order-refund.md) for the provider-specific parameters and requirements.

