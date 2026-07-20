# MailBluster: Update Product

Updates an existing product in MailBluster.

```
PUT https://connect.mindcloud.co/v1/universal/mailBluster/latest/actions/update-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailBluster `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mailBluster/latest/actions/update-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "productId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailBluster/latest/actions/update-product', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "productId": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `productId` | string | yes | Unique product ID to update. |
| `name` | string | yes | Updated product name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "product": {
        "createdAt": "string",
        "id": "string",
        "name": "Ava Chen",
        "updatedAt": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Operation result message. |
| `product` | object | Updated product. |
| `product.createdAt` | string | Creation timestamp. |
| `product.id` | string | Product ID. |
| `product.name` | string | Product name. |
| `product.updatedAt` | string | Last update timestamp. |

## Native endpoint

Through the native MailBluster API, this operation is `PUT /products/:productId` (base URL `https://api.mailbluster.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-product.md) for the provider-specific parameters and requirements.

