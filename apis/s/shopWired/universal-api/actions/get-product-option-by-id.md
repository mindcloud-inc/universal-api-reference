# ShopWired: Get a product option

Retrieves a product option from ShopWired by ID.

```
GET https://connect.mindcloud.co/v1/universal/shopWired/latest/actions/get-product-option-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ShopWired `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shopWired/latest/actions/get-product-option-by-id?connectionId=$CONNECTION_ID&productId=1&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "productId": "1",
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shopWired/latest/actions/get-product-option-by-id?${params}`, {
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
| `productId` | number | yes | ID of the product which the option is assigned to. |
| `id` | number | yes | ID of the product option. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "name": "Ava Chen",
      "sortOrder": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `name` | string |  |
| `sortOrder` | number |  |

## Native endpoint

Through the native ShopWired API, this operation is `GET /products/{product_id}/options/{id}` (base URL `https://api.ecommerceapi.uk/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product-option-by-id.md) for the provider-specific parameters and requirements.

