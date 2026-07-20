# BILL Payables & Receivables: Authenticate

Signs in to Bill.com and creates an API session.

```
POST https://connect.mindcloud.co/v1/universal/billcom/latest/actions/authenticate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BILL Payables & Receivables `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/billcom/latest/actions/authenticate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/billcom/latest/actions/authenticate', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BILL Payables & Receivables API returns.

## Native endpoint

Through the native BILL Payables & Receivables API, this operation is `POST Login.json` (base URL `https://api.bill.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/authenticate.md) for the provider-specific parameters and requirements.

