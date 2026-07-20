# MailBluster: Create Product

Creates a new product in MailBluster.

```
POST https://connect.mindcloud.co/v1/universal/mailBluster/latest/actions/create-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailBluster `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mailBluster/latest/actions/create-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "productId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailBluster/latest/actions/create-product', {
  method: 'POST',
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
| `productId` | string | yes | Unique product ID in MailBluster. |
| `name` | string | yes | Product name. |

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
| `product` | object | Created product. |
| `product.createdAt` | string | Creation timestamp. |
| `product.id` | string | Product ID. |
| `product.name` | string | Product name. |
| `product.updatedAt` | string | Last update timestamp. |

## Native endpoint

Through the native MailBluster API, this operation is `POST /products` (base URL `https://api.mailbluster.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-product.md) for the provider-specific parameters and requirements.

