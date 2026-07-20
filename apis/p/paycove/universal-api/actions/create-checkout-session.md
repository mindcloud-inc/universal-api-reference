# Paycove: Create Checkout Session

Creates a checkout session in Paycove.

```
POST https://connect.mindcloud.co/v1/universal/paycove/latest/actions/create-checkout-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paycove `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/paycove/latest/actions/create-checkout-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "aid": "string",
  "lineItems[]": [
    {}
  ],
  "orderId": "string",
  "templateId": 1,
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/paycove/latest/actions/create-checkout-session', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "aid": "string",
    "lineItems[]": [{}],
    "orderId": "string",
    "templateId": 1,
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `aid` | string | yes | The account identifier for the checkout session. |
| `cancelUrl` | string | no | Where the customer is redirected after cancelling checkout. |
| `contact` | object | no | Contact information for the checkout session. |
| `lineItems[]` | array<object> | yes | Line items to include in the checkout session. |
| `orderId` | string | yes | Your internal order ID for the checkout session. |
| `successUrl` | string | no | Where the customer is redirected after a successful payment. |
| `templateId` | number | yes | Template ID for the checkout session. |
| `type` | string | yes | Checkout type, such as invoice. |
| `webhookUrl` | string | no | Webhook URL for checkout updates. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "checkoutUrl": "https://example.com",
      "dealId": 1,
      "uniqueDealId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `checkoutUrl` | string |  |
| `dealId` | number |  |
| `uniqueDealId` | string |  |

## Native endpoint

Through the native Paycove API, this operation is `POST https://paycove.io/api/checkout/:aid` (base URL `https://paycove.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-checkout-session.md) for the provider-specific parameters and requirements.

