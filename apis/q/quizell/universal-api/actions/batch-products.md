# Quizell: Batch Products

Creates multiple products in Quizell.

```
POST https://connect.mindcloud.co/v1/universal/quizell/latest/actions/batch-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quizell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/quizell/latest/actions/batch-products" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "products": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quizell/latest/actions/batch-products', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "products": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `products` | object | yes | Array of product objects. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "status": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `status` | boolean |  |

## Native endpoint

Through the native Quizell API, this operation is `POST /products/batch` (base URL `https://api.quizell.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/batch-products.md) for the provider-specific parameters and requirements.

