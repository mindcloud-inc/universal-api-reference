# Reloadify: Create Or Update Shopping Cart

Creates or updates a shopping cart in Reloadify.

```
PUT https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/create-or-update-shopping-cart
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reloadify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/create-or-update-shopping-cart" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "languageId": "string",
  "shopping_cart.id": "string",
  "shopping_cart.profile_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/create-or-update-shopping-cart', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "languageId": "string",
    "shopping_cart.id": "string",
    "shopping_cart.profile_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `languageId` | string | yes | Reloadify language ID. |
| `shopping_cart.id` | string | yes | Shopping cart identifier. |
| `shopping_cart.profile_id` | string | yes | Existing Reloadify profile ID. |

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

Through the native Reloadify API, this operation is `PUT /v2/languages/:language_id/shopping_carts` (base URL `https://api.reloadify.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-shopping-cart.md) for the provider-specific parameters and requirements.

