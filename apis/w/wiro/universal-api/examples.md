# Wiro Universal API Examples

These examples use the MindCloud API key and Wiro connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Explore Models

Retrieves curated AI model collections from Wiro.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wiro/latest/actions/explore-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wiro/latest/actions/explore-models?${params}`, {
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
      "errors": [
        "string"
      ],
      "explore": [
        {}
      ],
      "result": true
    }
  ],
  "meta": {}
}
```

See the full [Explore Models action reference](actions/explore-models.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/wiro/latest/actions/explore-models).

## Cancel Task

Cancels a queued task in Wiro.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/wiro/latest/actions/cancel-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wiro/latest/actions/cancel-task', {
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
      "errors": [
        "string"
      ],
      "result": true
    }
  ],
  "meta": {}
}
```

See the full [Cancel Task action reference](actions/cancel-task.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/wiro/latest/actions/cancel-task).
