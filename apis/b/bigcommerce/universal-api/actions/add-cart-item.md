# BigCommerce: Add Cart Item



```
POST https://connect.mindcloud.co/v1/universal/bigcommerce/latest/actions/add-cart-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BigCommerce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bigcommerce/latest/actions/add-cart-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cartId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bigcommerce/latest/actions/add-cart-item', {
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
| `customItems[].listPrice` | string | no |  |
| `customItems[].name` | string | no |  |
| `customItems[].quantity` | number | no |  |
| `lineItems[].giftWrapping` | object | no |  |
| `lineItems[].giftWrapping.wrapDetails` | string | no |  |
| `lineItems[].listPrice` | string | no |  |
| `lineItems[].name` | string | no |  |
| `lineItems[].productId` | string | no |  |
| `lineItems[].variantId` | string | no |  |
| `cartId` | string | yes |  |
| `customItems[].sku` | string | no |  |
| `lineItems[]` | array | no |  |
| `lineItems[].giftWrapping.wrapTogether` | string | no |  |
| `lineItems[].quantity` | string | no |  |
| `customItems[]` | array | no |  |
| `giftCertificates[]` | array | no |  |
| `version` | number | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BigCommerce API returns.

## Native endpoint

Through the native BigCommerce API, this operation is `POST /v3/carts/:cartId/items` (base URL `https://api.bigcommerce.com/stores/{{credentials.storeHash}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-cart-item.md) for the provider-specific parameters and requirements.

