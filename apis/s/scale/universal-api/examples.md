# Scale Universal API Examples

These examples use the MindCloud API key and Scale connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Multiple Projects



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scale/latest/actions/get-multiple-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scale/latest/actions/get-multiple-projects?${params}`, {
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
      "projects": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Get Multiple Projects action reference](actions/get-multiple-projects.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/scale/latest/actions/get-multiple-projects).

## Cancel Batch



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/scale/latest/actions/cancel-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/scale/latest/actions/cancel-batch', {
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
  "data": [
    {
      "id": "string",
      "metadata": {},
      "name": "Ava Chen",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Cancel Batch action reference](actions/cancel-batch.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/scale/latest/actions/cancel-batch).
