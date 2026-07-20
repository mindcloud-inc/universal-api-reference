# Apilio Universal API Examples

These examples use the MindCloud API key and Apilio connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Boolean Variables



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apilio/latest/actions/list-boolean-variables?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/apilio/latest/actions/list-boolean-variables?${params}`, {
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
      "name": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "uuid": "string",
      "value": true
    }
  ],
  "meta": {}
}
```

See the full [List Boolean Variables action reference](actions/list-boolean-variables.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/apilio/latest/actions/list-boolean-variables).

## Evaluate Logicblock



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/apilio/latest/actions/evaluate-logicblock" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "uuid": "a40f21df-7707-4898-9688-69bf1f8dd184"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/apilio/latest/actions/evaluate-logicblock', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "uuid": "a40f21df-7707-4898-9688-69bf1f8dd184"
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
      "active": true,
      "evaluate": true,
      "name": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

See the full [Evaluate Logicblock action reference](actions/evaluate-logicblock.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/apilio/latest/actions/evaluate-logicblock).
