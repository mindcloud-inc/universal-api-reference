# Poof: Fetch Product

Retrieves product details from the Poof API.

```
GET https://connect.mindcloud.co/v1/universal/poof/latest/actions/fetch-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Poof `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/poof/latest/actions/fetch-product?connectionId=$CONNECTION_ID&product_id=e098921c-9db2-4796" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "product_id": "e098921c-9db2-4796"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/poof/latest/actions/fetch-product?${params}`, {
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
| `product_id` | string | yes | Product identifier. Default: `e098921c-9db2-4796`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "image": "string",
      "maxPurchase": "string",
      "minPurchase": "string",
      "price": "string",
      "productId": "string",
      "productName": "Ava Chen",
      "quantity": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `image` | string |  |
| `maxPurchase` | string |  |
| `minPurchase` | string |  |
| `price` | string |  |
| `productId` | string |  |
| `productName` | string |  |
| `quantity` | string |  |
| `username` | string |  |

## Native endpoint

Through the native Poof API, this operation is `POST /fetch_product` (base URL `https://www.poof.io/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-product.md) for the provider-specific parameters and requirements.

