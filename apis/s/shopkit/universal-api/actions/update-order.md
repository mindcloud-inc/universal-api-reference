# Shopkit: Update Order

Updates an existing order in Shopkit.

```
PUT https://connect.mindcloud.co/v1/universal/shopkit/latest/actions/update-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shopkit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/shopkit/latest/actions/update-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shopkit/latest/actions/update-order', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "client": {},
      "created_at": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "hash": "string",
      "id": 1,
      "paid": true,
      "payment": {},
      "permalink": "https://example.com",
      "products": [
        {}
      ],
      "shipping": {},
      "status": 1,
      "status_alias": "string",
      "subtotal": 1,
      "total": 1,
      "update_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `client` | object |  |
| `created_at` | date |  |
| `currency` | string |  |
| `hash` | string |  |
| `id` | number |  |
| `paid` | boolean |  |
| `payment` | object |  |
| `permalink` | string |  |
| `products` | array<object> |  |
| `shipping` | object |  |
| `status` | number |  |
| `status_alias` | string |  |
| `subtotal` | number |  |
| `total` | number |  |
| `update_at` | date |  |

## Native endpoint

Through the native Shopkit API, this operation is `PUT /order/:id` (base URL `https://api.shopk.it/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-order.md) for the provider-specific parameters and requirements.

