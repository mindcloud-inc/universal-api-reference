# Anthropic Universal API Examples

These examples use the MindCloud API key and Anthropic connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Models

Retrieves available API models from Anthropic.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/list-models?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/list-models?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "displayName": "Ava Chen",
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Models action reference](actions/list-models.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/anthropic/latest/actions/list-models).

## Cancel Message Batch

Cancels a message batch in Anthropic.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/cancel-message-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "messageBatchId": "msgbatch_123"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/cancel-message-batch', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "messageBatchId": "msgbatch_123"
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
      "archivedAt": "string",
      "cancelInitiatedAt": "string",
      "createdAt": "string",
      "endedAt": "string",
      "expiresAt": "string",
      "id": "string",
      "processingStatus": "string",
      "requestCounts": {},
      "resultsUrl": "https://example.com",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Cancel Message Batch action reference](actions/cancel-message-batch.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/anthropic/latest/actions/cancel-message-batch).
