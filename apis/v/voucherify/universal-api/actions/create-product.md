# Voucherify: Create Product

Creates a new product in Voucherify, or updates an existing one.

```
POST https://connect.mindcloud.co/v1/universal/voucherify/latest/actions/create-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voucherify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/voucherify/latest/actions/create-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/voucherify/latest/actions/create-product', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sourceId` | string | no | External product identifier. |
| `name` | string | no | Display name for the product. |
| `price` | number | no | Product price in minor currency units. |
| `imageUrl` | string | no | Image URL for the product. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": [
        "string"
      ],
      "createdAt": "string",
      "id": "string",
      "imageUrl": "https://example.com",
      "metadata": {},
      "name": "Ava Chen",
      "object": "string",
      "price": 1,
      "sourceId": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | array<string> |  |
| `createdAt` | string |  |
| `id` | string |  |
| `imageUrl` | string |  |
| `metadata` | object |  |
| `name` | string |  |
| `object` | string |  |
| `price` | number |  |
| `sourceId` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Voucherify API, this operation is `POST /products` (base URL `https://us1.api.voucherify.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-product.md) for the provider-specific parameters and requirements.

