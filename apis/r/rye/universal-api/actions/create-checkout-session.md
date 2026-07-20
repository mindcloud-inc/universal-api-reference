# Rye: Create Checkout Session

Creates a checkout session in Rye.

```
POST https://connect.mindcloud.co/v1/universal/rye/latest/actions/create-checkout-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rye `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rye/latest/actions/create-checkout-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "productUrl": "https://example.com",
  "quantity": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rye/latest/actions/create-checkout-session', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "productUrl": "https://example.com",
    "quantity": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `buyer` | object | no | Optional buyer information object. |
| `constraints` | object | no | Checkout constraints object. |
| `discoverPromoCodes` | boolean | no | Whether to discover promo codes automatically. |
| `layout` | string | no | Optional layout for the checkout UI. |
| `productUrl` | string | yes | Product URL to purchase. |
| `promoCodes[]` | array<string> | no | Promo codes to apply. Accepts multiple values as an array. |
| `quantity` | number | yes | Quantity to purchase. |
| `variantSelections[]` | array<object> | no | Variant selections to apply. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `url` | string |  |

## Native endpoint

Through the native Rye API, this operation is `POST /api/v1/betas/checkout-sessions` (base URL `https://staging.api.rye.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-checkout-session.md) for the provider-specific parameters and requirements.

