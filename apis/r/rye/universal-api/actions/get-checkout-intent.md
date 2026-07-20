# Rye: Get Checkout Intent

Retrieves a checkout intent from Rye.

```
GET https://connect.mindcloud.co/v1/universal/rye/latest/actions/get-checkout-intent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rye `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rye/latest/actions/get-checkout-intent?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rye/latest/actions/get-checkout-intent?${params}`, {
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
| `id` | string | yes | The checkout intent id. |

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

Through the native Rye API, this operation is `GET /api/v1/checkout-intents/{id}` (base URL `https://staging.api.rye.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-checkout-intent.md) for the provider-specific parameters and requirements.

