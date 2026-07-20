# Quo Universal API Examples

These examples use the MindCloud API key and Quo connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Call By ID

Retrieves a call from Quo by ID.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quo/latest/actions/get-call-by-id?connectionId=$CONNECTION_ID&callId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "callId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quo/latest/actions/get-call-by-id?${params}`, {
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
      "aiHandled": "string",
      "answeredAt": "2026-05-07T12:00:00.000Z",
      "answeredBy": "string",
      "callRoute": "string",
      "completedAt": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "direction": "string",
      "duration": 1,
      "forwardedFrom": "string",
      "forwardedTo": "string",
      "id": "string",
      "initiatedBy": "string",
      "participants": [
        "string"
      ],
      "phoneNumberId": "string",
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Call By ID action reference](actions/get-call-by-id.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/quo/latest/actions/get-call-by-id).

## Create Call Summary Webhook

Creates a new webhook for Quo call summaries.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/quo/latest/actions/create-call-summary-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "events[]": [
    "string"
  ],
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quo/latest/actions/create-call-summary-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "events[]": ["string"],
    "url": "https://example.com"
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "events": [
        "string"
      ],
      "id": "string",
      "key": "string",
      "label": "string",
      "orgId": "string",
      "resourceIds": [
        "string"
      ],
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Call Summary Webhook action reference](actions/create-call-summary-webhook.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/quo/latest/actions/create-call-summary-webhook).
