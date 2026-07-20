# Emporix Commerce Engine: List Cart Items

Retrieves items in a cart from Emporix Commerce Engine.

```
GET https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/list-cart-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Emporix Commerce Engine `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/list-cart-items?connectionId=$CONNECTION_ID&cartId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cartId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/list-cart-items?${params}`, {
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
| `cartId` | string | yes | The unique ID of the cart whose items should be listed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "calculatedPrice": {},
      "effectiveQuantity": 1,
      "id": "string",
      "itemYrn": "string",
      "metadata": {},
      "product": {},
      "quantity": 1,
      "totalTax": 1,
      "type": "string",
      "unitPrice": {},
      "yrn": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `calculatedPrice` | object |  |
| `effectiveQuantity` | number |  |
| `id` | string |  |
| `itemYrn` | string |  |
| `metadata` | object |  |
| `product` | object |  |
| `quantity` | number |  |
| `totalTax` | number |  |
| `type` | string |  |
| `unitPrice` | object |  |
| `yrn` | string |  |

## Native endpoint

Through the native Emporix Commerce Engine API, this operation is `GET /cart/{{credentials.tenantId}}/carts/:cartId/items` (base URL `https://api.emporix.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-cart-items.md) for the provider-specific parameters and requirements.

