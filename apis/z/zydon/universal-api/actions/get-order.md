# Zydon: Get Order

Retrieves order details from Zydon.

```
GET https://connect.mindcloud.co/v1/universal/zydon/latest/actions/get-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zydon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zydon/latest/actions/get-order?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zydon/latest/actions/get-order?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "items": [
        {}
      ],
      "partner_id": "string",
      "total_value": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Order identifier. |
| `items` | array<object> | Items included in the order. |
| `partner_id` | string | Partner identifier associated with the order. |
| `total_value` | number | Total value of the order. |

## Native endpoint

Through the native Zydon API, this operation is `GET /orders/{id}` (base URL `https://api.zydon.com.br/api/sales`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order.md) for the provider-specific parameters and requirements.

