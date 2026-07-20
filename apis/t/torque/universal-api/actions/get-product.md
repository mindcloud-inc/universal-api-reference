# Torque: Get Product



```
GET https://connect.mindcloud.co/v1/universal/torque/latest/actions/get-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Torque `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/torque/latest/actions/get-product?connectionId=$CONNECTION_ID&productId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "productId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/torque/latest/actions/get-product?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `productId` | string | yes | Torque product ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "createdAt": 1,
      "currency": "string",
      "description": "string",
      "id": "string",
      "image": "string",
      "inventory": 1,
      "isSubscription": true,
      "name": "Ava Chen",
      "price": 1,
      "requiresShipping": true,
      "sku": "string",
      "status": "string",
      "tags": [
        "string"
      ],
      "updatedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string |  |
| `createdAt` | number |  |
| `currency` | string |  |
| `description` | string |  |
| `id` | string |  |
| `image` | string |  |
| `inventory` | number |  |
| `isSubscription` | boolean |  |
| `name` | string |  |
| `price` | number |  |
| `requiresShipping` | boolean |  |
| `sku` | string |  |
| `status` | string |  |
| `tags` | array<string> |  |
| `updatedAt` | number |  |

## Native endpoint

Through the native Torque API, this operation is `GET /products/:productId` (base URL `https://app.torque.fi/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product.md) for the provider-specific parameters and requirements.

