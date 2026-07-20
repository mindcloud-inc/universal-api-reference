# Cohere Universal API Examples

These examples use the MindCloud API key and Cohere connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Models

Lists available AI models in Cohere.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cohere/latest/actions/list-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cohere/latest/actions/list-models?${params}`, {
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
      "models": [
        {}
      ],
      "nextPageToken": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Models action reference](actions/list-models.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cohere/latest/actions/list-models).

## Cancel Embed Job

Cancels an embed job in Cohere.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cohere/latest/actions/cancel-embed-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cohere/latest/actions/cancel-embed-job', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Cancel Embed Job action reference](actions/cancel-embed-job.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cohere/latest/actions/cancel-embed-job).
