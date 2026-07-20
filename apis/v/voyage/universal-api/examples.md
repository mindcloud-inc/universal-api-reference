# Voyage Universal API Examples

These examples use the MindCloud API key and Voyage connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Files

Retrieves files from Voyage.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voyage/latest/actions/list-files?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voyage/latest/actions/list-files?${params}`, {
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
      "bytes": 1,
      "createdAt": "string",
      "expiresAt": "string",
      "filename": "Ava Chen",
      "id": "string",
      "object": "string",
      "purpose": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Files action reference](actions/list-files.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/voyage/latest/actions/list-files).

## Cancel Batch

Cancels an in-progress batch in Voyage.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/voyage/latest/actions/cancel-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "batchId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/voyage/latest/actions/cancel-batch', {
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
      "cancelledAt": "string",
      "cancellingAt": "string",
      "completedAt": "string",
      "completionWindow": "string",
      "createdAt": "string",
      "endpoint": "string",
      "errorFileId": "string",
      "errors": {},
      "expectedCompletionAt": "string",
      "failedAt": "string",
      "finalizingAt": "string",
      "id": "string",
      "inProgressAt": "string",
      "inputFileId": "string",
      "metadata": {},
      "model": "string",
      "object": "string",
      "outputFileId": "string",
      "requestCounts": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Cancel Batch action reference](actions/cancel-batch.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/voyage/latest/actions/cancel-batch).
