# Agenthost.ai Universal API Examples

These examples use the MindCloud API key and Agenthost.ai connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get User Message Limit

Retrieves a user's message limit from Agenthost.ai.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agenthostai/latest/actions/get-user-message-limit?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agenthostai/latest/actions/get-user-message-limit?${params}`, {
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
      "limit": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get User Message Limit action reference](actions/get-user-message-limit.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/agenthostai/latest/actions/get-user-message-limit).

## Log In

Starts or completes Agenthost.ai login by email verification.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/agenthostai/latest/actions/log-in" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "user@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/agenthostai/latest/actions/log-in', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "user@example.com"
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

See the full [Log In action reference](actions/log-in.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/agenthostai/latest/actions/log-in).
