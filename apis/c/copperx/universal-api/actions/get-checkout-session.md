# Copperx: Get Checkout Session

Retrieves a checkout session from Copperx.

```
GET https://connect.mindcloud.co/v1/universal/copperx/latest/actions/get-checkout-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Copperx `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/copperx/latest/actions/get-checkout-session?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/copperx/latest/actions/get-checkout-session?${params}`, {
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
| `id` | string | yes | Checkout session ID path parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addresses": [
        {}
      ],
      "afterCompletion": "string",
      "amountDetails": {},
      "amountNet": "string",
      "amountSubtotal": "string",
      "amountTotal": "string",
      "createdAt": "string",
      "currency": "string",
      "customer": {},
      "customerCreation": "string",
      "customerDetails": {},
      "customerId": "string",
      "customerUpdate": {},
      "customFields": {},
      "discounts": [
        {}
      ],
      "expiresAt": "string",
      "id": "string",
      "isManualPayment": true,
      "lineItems": {},
      "mode": "string",
      "organizationId": "string",
      "paymentIntent": {},
      "paymentMethodTypes": [
        "string"
      ],
      "paymentSetting": {},
      "paymentStatus": "string",
      "status": "string",
      "submitType": "string",
      "successUrl": "https://example.com",
      "updatedAt": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addresses` | array<object> |  |
| `afterCompletion` | string |  |
| `amountDetails` | object |  |
| `amountNet` | string |  |
| `amountSubtotal` | string |  |
| `amountTotal` | string |  |
| `createdAt` | string |  |
| `currency` | string |  |
| `customer` | object |  |
| `customerCreation` | string |  |
| `customerDetails` | object |  |
| `customerId` | string |  |
| `customerUpdate` | object |  |
| `customFields` | object |  |
| `discounts` | array<object> |  |
| `expiresAt` | string |  |
| `id` | string |  |
| `isManualPayment` | boolean |  |
| `lineItems` | object |  |
| `mode` | string |  |
| `organizationId` | string |  |
| `paymentIntent` | object |  |
| `paymentMethodTypes` | array<string> |  |
| `paymentSetting` | object |  |
| `paymentStatus` | string |  |
| `status` | string |  |
| `submitType` | string |  |
| `successUrl` | string |  |
| `updatedAt` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Copperx API, this operation is `GET /checkout/sessions/{id}` (base URL `https://api.copperx.dev/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-checkout-session.md) for the provider-specific parameters and requirements.

