# Voucherify: Get Order

Retrieves an order from Voucherify.

```
GET https://connect.mindcloud.co/v1/universal/voucherify/latest/actions/get-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voucherify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voucherify/latest/actions/get-order?connectionId=$CONNECTION_ID&orderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orderId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voucherify/latest/actions/get-order?${params}`, {
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
| `orderId` | string | yes | Voucherify order identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "customer": {},
      "id": "string",
      "metadata": {},
      "object": "string",
      "sourceId": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `customer` | object |  |
| `id` | string |  |
| `metadata` | object |  |
| `object` | string |  |
| `sourceId` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Voucherify API, this operation is `GET /orders/:orderId` (base URL `https://us1.api.voucherify.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order.md) for the provider-specific parameters and requirements.

