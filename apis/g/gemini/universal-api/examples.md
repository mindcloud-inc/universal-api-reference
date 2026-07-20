# Gemini Universal API Examples

These examples use the MindCloud API key and Gemini connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Models

Retrieves a list of models from Gemini.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gemini/latest/actions/list-models?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gemini/latest/actions/list-models?${params}`, {
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
      "description": "string",
      "displayName": "Ava Chen",
      "inputTokenLimit": 1,
      "name": "Ava Chen",
      "outputTokenLimit": 1,
      "supportedGenerationMethods": [
        "string"
      ],
      "version": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Models action reference](actions/list-models.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/gemini/latest/actions/list-models).

## Async Batch Embed Content

Enqueues a batch embed content job in Gemini.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gemini/latest/actions/async-batch-embed-content" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "model": "gemini-embedding-001:asyncBatchEmbedContent",
  "batch": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gemini/latest/actions/async-batch-embed-content', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "model": "gemini-embedding-001:asyncBatchEmbedContent",
    "batch": "[object Object]"
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
      "metadata": {},
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Async Batch Embed Content action reference](actions/async-batch-embed-content.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/gemini/latest/actions/async-batch-embed-content).
