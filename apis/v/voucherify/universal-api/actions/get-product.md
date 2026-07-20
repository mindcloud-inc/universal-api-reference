# Voucherify: Get Product

Retrieves a product from Voucherify.

```
GET https://connect.mindcloud.co/v1/universal/voucherify/latest/actions/get-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voucherify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voucherify/latest/actions/get-product?connectionId=$CONNECTION_ID&productId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "productId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voucherify/latest/actions/get-product?${params}`, {
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
| `productId` | string | yes | Voucherify product identifier. |

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

Through the native Voucherify API, this operation is `GET /products/:productId` (base URL `https://us1.api.voucherify.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product.md) for the provider-specific parameters and requirements.

