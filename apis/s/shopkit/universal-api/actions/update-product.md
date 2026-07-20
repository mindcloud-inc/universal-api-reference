# Shopkit: Update Product

Updates an existing product in Shopkit.

```
PUT https://connect.mindcloud.co/v1/universal/shopkit/latest/actions/update-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shopkit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/shopkit/latest/actions/update-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shopkit/latest/actions/update-product', {
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
      "categories": [
        {}
      ],
      "created_at": "2026-05-07T12:00:00.000Z",
      "handle": "string",
      "id": 1,
      "image": {},
      "options": [
        {}
      ],
      "permalink": "https://example.com",
      "price": 1,
      "reference": "string",
      "status": 1,
      "status_alias": "string",
      "title": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categories` | array<object> |  |
| `created_at` | date |  |
| `handle` | string |  |
| `id` | number |  |
| `image` | object |  |
| `options` | array<object> |  |
| `permalink` | string |  |
| `price` | number |  |
| `reference` | string |  |
| `status` | number |  |
| `status_alias` | string |  |
| `title` | string |  |
| `updated_at` | date |  |
| `url` | string |  |

## Native endpoint

Through the native Shopkit API, this operation is `PUT /product/:id` (base URL `https://api.shopk.it/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-product.md) for the provider-specific parameters and requirements.

