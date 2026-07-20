# Billwerkplus: Create Invoice for Customer

Creates an invoice for a Billwerkplus customer.

```
POST https://connect.mindcloud.co/v1/universal/billwerkplus/latest/actions/create-invoice-for-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billwerkplus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/billwerkplus/latest/actions/create-invoice-for-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "handle": "string",
  "invoiceHandle": "string",
  "orderLines[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/billwerkplus/latest/actions/create-invoice-for-customer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "handle": "string",
    "invoiceHandle": "string",
    "orderLines[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `handle` | string | yes | Customer handle. |
| `invoiceHandle` | string | yes | Unique invoice handle. |
| `orderLines[]` | array<object> | yes | Invoice order lines. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Billwerkplus API returns.

## Native endpoint

Through the native Billwerkplus API, this operation is `POST /customer/:handle/invoice` (base URL `https://api.frisbii.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-invoice-for-customer.md) for the provider-specific parameters and requirements.

