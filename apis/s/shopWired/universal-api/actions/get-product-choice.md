# ShopWired: Get a product choice

Retrieves a product choice from ShopWired by ID.

```
GET https://connect.mindcloud.co/v1/universal/shopWired/latest/actions/get-product-choice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ShopWired `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shopWired/latest/actions/get-product-choice?connectionId=$CONNECTION_ID&productId=1&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "productId": "1",
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shopWired/latest/actions/get-product-choice?${params}`, {
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
| `productId` | number | yes | ID of the product. |
| `id` | number | yes | ID of the product choice. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "costPrice": 1,
      "customPrice": 1,
      "id": 1,
      "set": {
        "id": 1,
        "name": "Ava Chen"
      },
      "value": {
        "id": 1,
        "name": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `costPrice` | number |  |
| `customPrice` | number |  |
| `id` | number |  |
| `set.id` | number |  |
| `set.name` | string |  |
| `value.id` | number |  |
| `value.name` | string |  |

## Native endpoint

Through the native ShopWired API, this operation is `GET /products/{product_id}/choices/{id}` (base URL `https://api.ecommerceapi.uk/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product-choice.md) for the provider-specific parameters and requirements.

