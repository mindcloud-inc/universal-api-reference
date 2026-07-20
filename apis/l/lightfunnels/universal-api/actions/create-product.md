# Lightfunnels: Create Product



```
POST https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/create-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lightfunnels `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/create-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/create-product', {
  method: 'POST',
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
      "createProduct": {
        "id": "string",
        "name": "Ava Chen",
        "price": 1,
        "slug": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createProduct` | object | Created product. |
| `createProduct.id` | string | Product id. |
| `createProduct.name` | string | Product name. |
| `createProduct.price` | number | Product price. |
| `createProduct.slug` | string | Product slug. |

## Native endpoint

Through the native Lightfunnels API, this operation is `POST /api/v2` (base URL `https://services.lightfunnels.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-product.md) for the provider-specific parameters and requirements.

