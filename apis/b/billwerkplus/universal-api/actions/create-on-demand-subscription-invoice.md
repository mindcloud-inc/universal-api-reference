# Billwerkplus: Create On-Demand Subscription Invoice

Creates an on-demand invoice for a Billwerkplus subscription.

```
POST https://connect.mindcloud.co/v1/universal/billwerkplus/latest/actions/create-on-demand-subscription-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billwerkplus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/billwerkplus/latest/actions/create-on-demand-subscription-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "handle": "string",
  "invoiceHandle": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/billwerkplus/latest/actions/create-on-demand-subscription-invoice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "handle": "string",
    "invoiceHandle": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `handle` | string | yes | Subscription handle. |
| `invoiceHandle` | string | yes | Unique invoice handle. |
| `instant` | boolean | no | Process the invoice immediately. Default: `false`. |
| `planManual` | boolean | no | Generate plan order lines manually for the invoice. Default: `false`. |
| `planPeriodFrom` | string | no | Service period start for manually generated plan lines. |
| `planPeriodTo` | string | no | Service period end for manually generated plan lines. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Billwerkplus API returns.

## Native endpoint

Through the native Billwerkplus API, this operation is `POST /subscription/:handle/invoice` (base URL `https://api.frisbii.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-on-demand-subscription-invoice.md) for the provider-specific parameters and requirements.

