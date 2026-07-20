# boomApp Connect Universal API Examples

These examples use the MindCloud API key and boomApp Connect connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Retrieve Message Responses

Retrieves responses to outbound messages from boomApp Connect.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/boomAppConnect/latest/actions/retrieve-message-responses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/boomAppConnect/latest/actions/retrieve-message-responses?${params}`, {
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
      "hasMore": true,
      "message": "string",
      "replies": {
        "campaignName": "Ava Chen",
        "conversationId": "string",
        "customParameter": "string",
        "from": "string",
        "isNew": true,
        "responseContent": "string",
        "responseDate": "string",
        "responseId": "string",
        "transactionDate": "string",
        "transactionId": "string"
      },
      "status": 1
    }
  ],
  "meta": {}
}
```

See the full [Retrieve Message Responses action reference](actions/retrieve-message-responses.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/boomAppConnect/latest/actions/retrieve-message-responses).

## Create Masked Two-Way SMS Thread

Creates a masked two-way SMS thread in boomApp Connect.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/boomAppConnect/latest/actions/create-masked-two-way-sms-thread" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "from": "447890123456",
  "to": "447890123456",
  "reference": "reference-id",
  "message": "Initial message text"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/boomAppConnect/latest/actions/create-masked-two-way-sms-thread', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "from": "447890123456",
    "to": "447890123456",
    "reference": "reference-id",
    "message": "Initial message text"
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
      "message": "string",
      "status": 1,
      "threadId": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Masked Two-Way SMS Thread action reference](actions/create-masked-two-way-sms-thread.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/boomAppConnect/latest/actions/create-masked-two-way-sms-thread).
