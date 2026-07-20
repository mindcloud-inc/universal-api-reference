# Groq Universal API Examples

These examples use the MindCloud API key and Groq connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Models

Retrieves models from Groq.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/groq/latest/actions/list-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/groq/latest/actions/list-models?${params}`, {
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
      "active": true,
      "contextWindow": 1,
      "created": 1,
      "id": "string",
      "maxCompletionTokens": 1,
      "object": "string",
      "ownedBy": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Models action reference](actions/list-models.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/groq/latest/actions/list-models).

## Cancel Batch

Cancels a batch in Groq.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/groq/latest/actions/cancel-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "batchId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/groq/latest/actions/cancel-batch', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "batchId": "string"
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
      "cancelledAt": 1,
      "cancellingAt": 1,
      "completedAt": 1,
      "completionWindow": "string",
      "createdAt": 1,
      "endpoint": "string",
      "errorFileId": "string",
      "errors": {},
      "expiredAt": 1,
      "expiresAt": 1,
      "failedAt": 1,
      "finalizingAt": 1,
      "id": "string",
      "inProgressAt": 1,
      "inputFileId": "string",
      "metadata": {},
      "object": "string",
      "outputFileId": "string",
      "requestCounts": {
        "completed": 1,
        "failed": 1,
        "total": 1
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Cancel Batch action reference](actions/cancel-batch.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/groq/latest/actions/cancel-batch).
