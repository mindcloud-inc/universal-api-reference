# Rye: Add Payment To Checkout Intent



```
PUT https://connect.mindcloud.co/v1/universal/rye/latest/actions/add-payment-to-checkout-intent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rye `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rye/latest/actions/add-payment-to-checkout-intent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "paymentMethod": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rye/latest/actions/add-payment-to-checkout-intent', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "paymentMethod": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The checkout intent id. |
| `paymentMethod` | object | yes | Payment method object. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "buyer": {},
      "constraints": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "discoverPromoCodes": true,
      "failureReason": {},
      "id": "string",
      "nextAction": {},
      "offer": {},
      "orderId": "string",
      "paymentMethod": {},
      "productUrl": "https://example.com",
      "promoCodes": [
        "string"
      ],
      "quantity": 1,
      "state": "string",
      "variantSelections": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `buyer` | object |  |
| `constraints` | object |  |
| `createdAt` | date |  |
| `discoverPromoCodes` | boolean |  |
| `failureReason` | object |  |
| `id` | string |  |
| `nextAction` | object |  |
| `offer` | object |  |
| `orderId` | string |  |
| `paymentMethod` | object |  |
| `productUrl` | string |  |
| `promoCodes` | array<string> |  |
| `quantity` | number |  |
| `state` | string |  |
| `variantSelections` | array<object> |  |

## Native endpoint

Through the native Rye API, this operation is `POST /api/v1/checkout-intents/{id}/payment` (base URL `https://staging.api.rye.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-payment-to-checkout-intent.md) for the provider-specific parameters and requirements.

