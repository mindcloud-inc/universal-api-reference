# Torque: Get Products



```
GET https://connect.mindcloud.co/v1/universal/torque/latest/actions/get-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Torque `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/torque/latest/actions/get-products?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/torque/latest/actions/get-products?${params}`, {
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
| `status` | list | no | Optional product status filter: active, inactive, draft, or archived. One of: `0`, `1`, `2`, `3`. |

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

Through the native Torque API, this operation is `GET /products` (base URL `https://app.torque.fi/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-products.md) for the provider-specific parameters and requirements.

