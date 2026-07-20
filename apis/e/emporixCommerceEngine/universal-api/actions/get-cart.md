# Emporix Commerce Engine: Get Cart

Retrieves a cart from Emporix Commerce Engine.

```
GET https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/get-cart
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Emporix Commerce Engine `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/get-cart?connectionId=$CONNECTION_ID&cartId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cartId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/get-cart?${params}`, {
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
| `cartId` | string | yes | The unique ID of the cart. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "calculatedPrice": {},
      "currency": "string",
      "customerId": "string",
      "id": "string",
      "items": [
        {}
      ],
      "legalEntityId": "string",
      "metadata": {},
      "orderId": "string",
      "quoteId": "string",
      "siteCode": "string",
      "totalPrice": {},
      "totalUnitsCount": 1,
      "type": "string",
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
| `currency` | string |  |
| `customerId` | string |  |
| `id` | string |  |
| `items` | array<object> |  |
| `legalEntityId` | string |  |
| `metadata` | object |  |
| `orderId` | string |  |
| `quoteId` | string |  |
| `siteCode` | string |  |
| `totalPrice` | object |  |
| `totalUnitsCount` | number |  |
| `type` | string |  |
| `yrn` | string |  |

## Native endpoint

Through the native Emporix Commerce Engine API, this operation is `GET /cart/{{credentials.tenantId}}/carts/:cartId` (base URL `https://api.emporix.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-cart.md) for the provider-specific parameters and requirements.

