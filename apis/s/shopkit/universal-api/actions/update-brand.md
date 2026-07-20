# Shopkit: Update Brand

Updates an existing brand in Shopkit.

```
PUT https://connect.mindcloud.co/v1/universal/shopkit/latest/actions/update-brand
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shopkit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/shopkit/latest/actions/update-brand" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shopkit/latest/actions/update-brand', {
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
      "active": true,
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "handle": "string",
      "id": 1,
      "image": {},
      "num_products": 1,
      "permalink": "https://example.com",
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
| `active` | boolean |  |
| `created_at` | date |  |
| `description` | string |  |
| `handle` | string |  |
| `id` | number |  |
| `image` | object |  |
| `num_products` | number |  |
| `permalink` | string |  |
| `title` | string |  |
| `updated_at` | date |  |
| `url` | string |  |

## Native endpoint

Through the native Shopkit API, this operation is `PUT /brand/:id` (base URL `https://api.shopk.it/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-brand.md) for the provider-specific parameters and requirements.

