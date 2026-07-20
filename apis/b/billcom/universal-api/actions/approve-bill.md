# BILL Payables & Receivables: Approve Bill

Approves a bill in Bill.com.

```
POST https://connect.mindcloud.co/v1/universal/billcom/latest/actions/approve-bill
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BILL Payables & Receivables `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/billcom/latest/actions/approve-bill" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "objectId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/billcom/latest/actions/approve-bill', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "objectId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `objectId` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BILL Payables & Receivables API returns.

## Native endpoint

Through the native BILL Payables & Receivables API, this operation is `POST Approve.json` (base URL `https://api.bill.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/approve-bill.md) for the provider-specific parameters and requirements.

