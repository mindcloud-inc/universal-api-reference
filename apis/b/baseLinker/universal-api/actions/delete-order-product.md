# BaseLinker: Delete Order Product

Deletes a product from an order in BaseLinker.

```
DELETE https://connect.mindcloud.co/v1/universal/baseLinker/latest/actions/delete-order-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BaseLinker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/baseLinker/latest/actions/delete-order-product?connectionId=$CONNECTION_ID&order_id=1&order_product_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "order_id": "1",
  "order_product_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/baseLinker/latest/actions/delete-order-product?${params}`, {
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
| `order_id` | number | yes | Order identifier. |
| `order_product_id` | number | yes | Order product line identifier to remove. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string | SUCCESS when the order item was deleted. |

## Native endpoint

Through the native BaseLinker API, this operation is `POST /connector.php` (base URL `https://api.baselinker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-order-product.md) for the provider-specific parameters and requirements.

