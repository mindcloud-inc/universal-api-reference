# Revi.io Reviews: Create Products

Creates products in Revi.io Reviews.

```
POST https://connect.mindcloud.co/v1/universal/reviioReviews/latest/actions/create-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Revi.io Reviews `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/reviioReviews/latest/actions/create-products" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "products[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/reviioReviews/latest/actions/create-products', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "products[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `products[]` | array<object> | yes | Array of Revi product objects to create or update. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "product_count": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `product_count` | number | Number of products processed by Revi. |
| `success` | boolean | Whether the products payload was accepted. |

## Native endpoint

Through the native Revi.io Reviews API, this operation is `POST /products` (base URL `https://api.revi.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-products.md) for the provider-specific parameters and requirements.

