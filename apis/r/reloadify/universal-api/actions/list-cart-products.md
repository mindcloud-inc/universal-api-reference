# Reloadify: List Cart Products

Retrieves products for a shopping cart in Reloadify.

```
GET https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/list-cart-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reloadify `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/list-cart-products?connectionId=$CONNECTION_ID&limit=25&offset=0&languageId=string&shoppingCartId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "languageId": "string",
  "shoppingCartId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/list-cart-products?${params}`, {
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
| `shoppingCartId` | string | yes | Shopping cart identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "product_id": "string",
      "shopping_cart_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `product_id` | string |  |
| `shopping_cart_id` | string |  |

## Native endpoint

Through the native Reloadify API, this operation is `GET /v2/languages/:language_id/shopping_carts/:shopping_cart_id/products` (base URL `https://api.reloadify.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-cart-products.md) for the provider-specific parameters and requirements.

