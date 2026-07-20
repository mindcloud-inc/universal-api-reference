# Encodian - Sign Universal API Examples

These examples use the MindCloud API key and Encodian - Sign connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Trigr Subscription Status



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/encodianSign/latest/actions/get-trigr-subscription-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/encodianSign/latest/actions/get-trigr-subscription-status?${params}`, {
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
  "data": [
    {
      "availableActionsMonth": 1,
      "availableActionsMonthDec": 1,
      "billingInterval": "string",
      "Errors": [
        "string"
      ],
      "expiryDate": "2026-05-07T12:00:00.000Z",
      "HttpStatusCode": 1,
      "HttpStatusMessage": "string",
      "monthlyActions": 1,
      "OperationId": "string",
      "OperationStatus": "string",
      "subscriptionEnabled": true,
      "subscriptionLevel": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Trigr Subscription Status action reference](actions/get-trigr-subscription-status.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/encodianSign/latest/actions/get-trigr-subscription-status).

## Create Trigr Webhook Subscription



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/encodianSign/latest/actions/create-trigr-webhook-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "callbackUrl": "https://example.com",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/encodianSign/latest/actions/create-trigr-webhook-subscription', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "callbackUrl": "https://example.com",
    "title": "string"
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
      "Errors": [
        "string"
      ],
      "HttpStatusCode": 1,
      "HttpStatusMessage": "string",
      "success": true,
      "tenantWebHookId": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Trigr Webhook Subscription action reference](actions/create-trigr-webhook-subscription.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/encodianSign/latest/actions/create-trigr-webhook-subscription).
