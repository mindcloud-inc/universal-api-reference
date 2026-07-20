# Understory: List Order Refunds

Retrieves order refunds from Understory.

```
GET https://connect.mindcloud.co/v1/universal/understory/latest/actions/list-order-refunds
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Understory `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/understory/latest/actions/list-order-refunds?connectionId=$CONNECTION_ID&orderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orderId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/understory/latest/actions/list-order-refunds?${params}`, {
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
| `orderId` | string | yes | The unique identifier of the order. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {
          "amount": {
            "currency": "string",
            "exponent": 1,
            "value": 1
          },
          "created_at": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "status": "string",
          "transaction_id": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items[].amount.currency` | string |  |
| `items[].amount.exponent` | number |  |
| `items[].amount.value` | number |  |
| `items[].created_at` | date |  |
| `items[].id` | string |  |
| `items[].status` | string |  |
| `items[].transaction_id` | string |  |

## Native endpoint

Through the native Understory API, this operation is `GET /v1/orders/{{orderId}}/refunds` (base URL `https://api.understory.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-order-refunds.md) for the provider-specific parameters and requirements.

