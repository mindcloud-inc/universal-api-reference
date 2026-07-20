# Paystack: Create Subscription



```
POST https://connect.mindcloud.co/v1/universal/paystack/latest/actions/create-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paystack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/paystack/latest/actions/create-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customer": "string",
  "plan": "string",
  "authorization": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/paystack/latest/actions/create-subscription', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customer": "string",
    "plan": "string",
    "authorization": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customer` | string | yes |  |
| `plan` | string | yes |  |
| `authorization` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "cron_expression": "string",
      "customer": {},
      "email_token": "ava@example.com",
      "id": 1,
      "next_payment_date": "string",
      "open_invoice": {},
      "plan": {},
      "status": "string",
      "subscription_code": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `cron_expression` | string |  |
| `customer` | object |  |
| `email_token` | string |  |
| `id` | number |  |
| `next_payment_date` | string |  |
| `open_invoice` | object |  |
| `plan` | object |  |
| `status` | string |  |
| `subscription_code` | string |  |

## Native endpoint

Through the native Paystack API, this operation is `POST /subscription` (base URL `https://api.paystack.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-subscription.md) for the provider-specific parameters and requirements.

