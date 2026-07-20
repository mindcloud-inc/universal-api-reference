# ShopWired: Get a specific product variation

Retrieves a product variation from ShopWired by ID.

```
GET https://connect.mindcloud.co/v1/universal/shopWired/latest/actions/get-product-variation-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ShopWired `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shopWired/latest/actions/get-product-variation-by-id?connectionId=$CONNECTION_ID&productId=1&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "productId": "1",
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shopWired/latest/actions/get-product-variation-by-id?${params}`, {
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
| `productId` | number | yes | The unique identifier of the product. |
| `id` | number | yes | The unique identifier of the product variation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "costPrice": 1,
      "id": 1,
      "price": 1,
      "salePrice": 1,
      "sku": "string",
      "stock": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `costPrice` | number |  |
| `id` | number |  |
| `price` | number |  |
| `salePrice` | number |  |
| `sku` | string |  |
| `stock` | number |  |
| `url` | string |  |

## Native endpoint

Through the native ShopWired API, this operation is `GET /products/{product_id}/variations/{id}` (base URL `https://api.ecommerceapi.uk/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product-variation-by-id.md) for the provider-specific parameters and requirements.

