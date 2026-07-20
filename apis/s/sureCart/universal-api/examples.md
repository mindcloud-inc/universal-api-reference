# SureCart Universal API Examples

These examples use the MindCloud API key and SureCart connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Retrieve Account



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/retrieve-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/retrieve-account?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Retrieve Account action reference](actions/retrieve-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sureCart/latest/actions/retrieve-account).

## Cancel/Pause Subscription



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/cancel-pause-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "cc7985b7-6738-45e2-8910-146bc0582404"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/cancel-pause-subscription', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "cc7985b7-6738-45e2-8910-146bc0582404"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "cancelAtPeriodEnd": true,
      "createdAt": 1,
      "currency": "string",
      "currentCancellationAct": "string",
      "currentPeriod": "string",
      "currentPeriodEndAt": 1,
      "currentPeriodStartAt": 1,
      "customer": "string",
      "endBehavior": "string",
      "id": "string",
      "liveMode": true,
      "manualPayment": true,
      "metadata": {},
      "object": "string",
      "pendingUpdate": {},
      "portalUrl": "https://example.com",
      "price": "string",
      "purchase": "string",
      "quantity": 1,
      "status": "string",
      "subtotalAmount": 1,
      "taxEnabled": true,
      "updatedAt": 1
    }
  ],
  "meta": {}
}
```

See the full [Cancel/Pause Subscription action reference](actions/cancel-pause-subscription.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sureCart/latest/actions/cancel-pause-subscription).
