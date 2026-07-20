# xAI Universal API Examples

These examples use the MindCloud API key and xAI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Models

Retrieves models from the xAI API.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xAI/latest/actions/list-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xAI/latest/actions/list-models?${params}`, {
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

See the full [List Models action reference](actions/list-models.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/xAI/latest/actions/list-models).

## Add Batch Requests

Adds batch requests in the xAI API.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/xAI/latest/actions/add-batch-requests" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xAI/latest/actions/add-batch-requests', {
  method: 'POST',
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
  "data": [
    {
      "batch_request_metadata": [
        {}
      ],
      "results": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Add Batch Requests action reference](actions/add-batch-requests.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/xAI/latest/actions/add-batch-requests).
