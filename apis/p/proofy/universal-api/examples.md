# Proofy Universal API Examples

These examples use the MindCloud API key and Proofy connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Check Batch Status



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/proofy/latest/actions/check-batch-status?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/proofy/latest/actions/check-batch-status?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [Check Batch Status action reference](actions/check-batch-status.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/proofy/latest/actions/check-batch-status).

## Create Batch Request



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/proofy/latest/actions/create-batch-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "emails[]": [
    "ava@example.com"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/proofy/latest/actions/create-batch-request', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "emails[]": ["ava@example.com"]
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

See the full [Create Batch Request action reference](actions/create-batch-request.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/proofy/latest/actions/create-batch-request).
