# Google AI Studio Universal API Examples

These examples use the MindCloud API key and Google AI Studio connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Models

Retrieves available Gemini models from Google AI Studio.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleAIStudio/latest/actions/list-models?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleAIStudio/latest/actions/list-models?${params}`, {
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

See the full [List Models action reference](actions/list-models.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/googleAIStudio/latest/actions/list-models).

## Cancel Batch

Cancels a batch operation in Google AI Studio.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/googleAIStudio/latest/actions/cancel-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "batches/1234567890"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleAIStudio/latest/actions/cancel-batch', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "batches/1234567890"
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
      "value": {}
    }
  ],
  "meta": {}
}
```

See the full [Cancel Batch action reference](actions/cancel-batch.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/googleAIStudio/latest/actions/cancel-batch).
