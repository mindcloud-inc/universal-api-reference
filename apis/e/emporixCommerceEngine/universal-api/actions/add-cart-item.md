# Emporix Commerce Engine: Add Cart Item

Adds an item to a cart in Emporix Commerce Engine.

```
POST https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/add-cart-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Emporix Commerce Engine `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/add-cart-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cartId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/add-cart-item', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cartId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cartId` | string | yes | The unique ID of the cart to add an item to. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "itemId": "string",
      "yrn": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `itemId` | string |  |
| `yrn` | string |  |

## Native endpoint

Through the native Emporix Commerce Engine API, this operation is `POST /cart/{{credentials.tenantId}}/carts/:cartId/items` (base URL `https://api.emporix.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-cart-item.md) for the provider-specific parameters and requirements.

