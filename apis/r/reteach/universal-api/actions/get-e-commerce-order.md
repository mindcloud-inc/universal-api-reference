# Reteach: Get E-Commerce Order



```
GET https://connect.mindcloud.co/v1/universal/reteach/latest/actions/get-e-commerce-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reteach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reteach/latest/actions/get-e-commerce-order?connectionId=$CONNECTION_ID&orderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orderId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reteach/latest/actions/get-e-commerce-order?${params}`, {
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
| `orderId` | string | yes | The id of the e-commerce order. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "committedAt": "string",
      "courses": [
        {}
      ],
      "customer": {},
      "id": "string",
      "number": "string",
      "quantity": 1,
      "totalAmount": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `committedAt` | string |  |
| `courses` | array<object> |  |
| `customer` | object |  |
| `id` | string |  |
| `number` | string |  |
| `quantity` | number |  |
| `totalAmount` | number |  |
| `url` | string |  |

## Native endpoint

Through the native Reteach API, this operation is `GET /v1/order/{orderId}` (base URL `https://api.reteach.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-e-commerce-order.md) for the provider-specific parameters and requirements.

