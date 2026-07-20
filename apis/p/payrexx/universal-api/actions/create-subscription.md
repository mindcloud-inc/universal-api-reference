# Payrexx: Create Subscription

Creates a subscription in Payrexx.

```
POST https://connect.mindcloud.co/v1/universal/payrexx/latest/actions/create-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Payrexx `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/payrexx/latest/actions/create-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userId": 1,
  "psp": 1,
  "amount": 1,
  "currency": "string",
  "purpose": "string",
  "paymentInterval": "string",
  "period": "string",
  "cancellationInterval": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/payrexx/latest/actions/create-subscription', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userId": 1,
    "psp": 1,
    "amount": 1,
    "currency": "string",
    "purpose": "string",
    "paymentInterval": "string",
    "period": "string",
    "cancellationInterval": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | number | yes | Webhook contact id for the subscription customer. |
| `psp` | number | yes | PSP id to use for the subscription. |
| `amount` | number | yes | Subscription amount in cents. |
| `currency` | string | yes | Subscription currency. |
| `purpose` | string | yes | Subscription payment purpose. |
| `paymentInterval` | string | yes | Subscription payment interval in PHP date interval format. |
| `period` | string | yes | Subscription period in PHP date interval format. |
| `cancellationInterval` | string | yes | Subscription cancellation interval in PHP date interval format. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Payrexx API returns.

## Native endpoint

Through the native Payrexx API, this operation is `POST Subscription/` (base URL `https://api.payrexx.com/v1.14/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-subscription.md) for the provider-specific parameters and requirements.

