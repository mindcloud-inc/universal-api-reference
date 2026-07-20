# Reloadify: List Order Products

Retrieves products for an order in Reloadify.

```
GET https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/list-order-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reloadify `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/list-order-products?connectionId=$CONNECTION_ID&limit=25&offset=0&languageId=string&orderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "languageId": "string",
  "orderId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/list-order-products?${params}`, {
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
| `languageId` | string | yes | Reloadify language ID. |
| `orderId` | string | yes | Order identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "custom_attributes": [
        {}
      ],
      "order_id": "string",
      "product_id": "string",
      "quantity": 1,
      "variant_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `custom_attributes` | array<object> |  |
| `order_id` | string |  |
| `product_id` | string |  |
| `quantity` | number |  |
| `variant_id` | string |  |

## Native endpoint

Through the native Reloadify API, this operation is `GET /v2/languages/:language_id/orders/:order_id/products` (base URL `https://api.reloadify.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-order-products.md) for the provider-specific parameters and requirements.

