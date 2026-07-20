# Reloadify: Get Shopping Cart

Retrieves a shopping cart from Reloadify.

```
GET https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/get-shopping-cart
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reloadify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/get-shopping-cart?connectionId=$CONNECTION_ID&languageId=string&shoppingCartId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "languageId": "string",
  "shoppingCartId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/get-shopping-cart?${params}`, {
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
      "created_at": "string",
      "currency": "string",
      "custom_attributes": [
        {}
      ],
      "deleted": true,
      "id": "string",
      "price": 1,
      "product_ids": [
        "string"
      ],
      "profile_id": "string",
      "recovery_token": "string",
      "recovery_url": "https://example.com",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `currency` | string |  |
| `custom_attributes` | array<object> |  |
| `deleted` | boolean |  |
| `id` | string |  |
| `price` | number |  |
| `product_ids` | array<string> |  |
| `profile_id` | string |  |
| `recovery_token` | string |  |
| `recovery_url` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native Reloadify API, this operation is `GET /v2/languages/:language_id/shopping_carts/:shopping_cart_id` (base URL `https://api.reloadify.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-shopping-cart.md) for the provider-specific parameters and requirements.

