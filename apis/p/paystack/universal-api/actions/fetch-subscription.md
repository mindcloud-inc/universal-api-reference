# Paystack: Fetch Subscription



```
GET https://connect.mindcloud.co/v1/universal/paystack/latest/actions/fetch-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paystack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paystack/latest/actions/fetch-subscription?connectionId=$CONNECTION_ID&subscriptionIdOrCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "subscriptionIdOrCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paystack/latest/actions/fetch-subscription?${params}`, {
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
| `subscriptionIdOrCode` | string | yes |  |

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

Through the native Paystack API, this operation is `GET /subscription/:subscriptionIdOrCode` (base URL `https://api.paystack.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-subscription.md) for the provider-specific parameters and requirements.

