# AgentX Universal API Examples

These examples use the MindCloud API key and AgentX connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get User Profile

Retrieves the current user profile from AgentX.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agentX/latest/actions/get-user-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agentX/latest/actions/get-user-profile?${params}`, {
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

See the full [Get User Profile action reference](actions/get-user-profile.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/agentX/latest/actions/get-user-profile).

## Add Conversation Context

Updates conversation context in AgentX without triggering chat.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/agentX/latest/actions/add-conversation-context" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "conversationId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/agentX/latest/actions/add-conversation-context', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "conversationId": "string"
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

See the full [Add Conversation Context action reference](actions/add-conversation-context.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/agentX/latest/actions/add-conversation-context).
