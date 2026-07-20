# Encodian - General Universal API Examples

These examples use the MindCloud API key and Encodian - General connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Subscription Flowr And Vertr Status

Retrieves Flowr and Vertr subscription status from Encodian.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/encodianGeneral/latest/actions/subscription-flowr-and-vertr-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/encodianGeneral/latest/actions/subscription-flowr-and-vertr-status?${params}`, {
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

See the full [Subscription Flowr And Vertr Status action reference](actions/subscription-flowr-and-vertr-status.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/encodianGeneral/latest/actions/subscription-flowr-and-vertr-status).

## AI Run Prompt Text

Runs a custom AI text prompt in Encodian.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/encodianGeneral/latest/actions/ai-run-prompt-text" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "model": "GPT_4_1_mini",
  "prompt": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/encodianGeneral/latest/actions/ai-run-prompt-text', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "model": "GPT_4_1_mini",
    "prompt": "string"
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
      "conversation": "string",
      "Errors": [
        "string"
      ],
      "HttpStatusCode": 1,
      "HttpStatusMessage": "string",
      "message": "string",
      "OperationId": "string",
      "OperationStatus": "string"
    }
  ],
  "meta": {}
}
```

See the full [AI Run Prompt Text action reference](actions/ai-run-prompt-text.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/encodianGeneral/latest/actions/ai-run-prompt-text).
