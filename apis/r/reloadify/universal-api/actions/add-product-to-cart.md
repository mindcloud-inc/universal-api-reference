# Reloadify: Add Product To Cart

Adds a product to a shopping cart in Reloadify.

```
PUT https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/add-product-to-cart
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reloadify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/add-product-to-cart" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "languageId": "string",
  "shoppingCartId": "string",
  "productId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/add-product-to-cart', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "languageId": "string",
    "shoppingCartId": "string",
    "productId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `languageId` | string | yes | Reloadify language ID. |
| `shoppingCartId` | string | yes | Shopping cart identifier. |
| `productId` | string | yes | Product identifier. |

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

Through the native Reloadify API, this operation is `PUT /v2/languages/:language_id/shopping_carts/:shopping_cart_id/products/:product_id` (base URL `https://api.reloadify.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-product-to-cart.md) for the provider-specific parameters and requirements.

