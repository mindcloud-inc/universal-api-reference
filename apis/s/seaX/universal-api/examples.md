# SeaX Universal API Examples

These examples use the MindCloud API key and SeaX connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List API Keys

Retrieves API keys from the current SeaX workspace.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seaX/latest/actions/list-api-keys?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seaX/latest/actions/list-api-keys?${params}`, {
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
      "total": 1
    }
  ],
  "meta": {}
}
```

See the full [List API Keys action reference](actions/list-api-keys.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/seaX/latest/actions/list-api-keys).

## Callback Auto Dialer Campaign Execution



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/seaX/latest/actions/callback-auto-dialer-campaign-execution" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/seaX/latest/actions/callback-auto-dialer-campaign-execution', {
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
      "answered_by": {},
      "attempt": 1,
      "created_time": "string",
      "end_time": "string",
      "id": "string",
      "logs": "string",
      "sequence": 1,
      "start_time": "string",
      "status": {},
      "updated_time": "string",
      "user_account": "string"
    }
  ],
  "meta": {}
}
```

See the full [Callback Auto Dialer Campaign Execution action reference](actions/callback-auto-dialer-campaign-execution.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/seaX/latest/actions/callback-auto-dialer-campaign-execution).
