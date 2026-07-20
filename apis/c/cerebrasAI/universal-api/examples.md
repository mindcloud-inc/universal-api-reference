# Cerebras AI Universal API Examples

These examples use the MindCloud API key and Cerebras AI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Models

Retrieves models from Cerebras AI.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cerebrasAI/latest/actions/list-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cerebrasAI/latest/actions/list-models?${params}`, {
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
      "data": [
        {}
      ],
      "object": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Models action reference](actions/list-models.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cerebrasAI/latest/actions/list-models).

## Create Batch

Creates a batch in Cerebras AI.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cerebrasAI/latest/actions/create-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "inputFileId": "string",
  "endpoint": "string",
  "completionWindow": "24h"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cerebrasAI/latest/actions/create-batch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "inputFileId": "string",
    "endpoint": "string",
    "completionWindow": "24h"
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
      "completionWindow": "string",
      "createdAt": 1,
      "endpoint": "string",
      "id": "string",
      "inputFileId": "string",
      "object": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Batch action reference](actions/create-batch.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cerebrasAI/latest/actions/create-batch).
