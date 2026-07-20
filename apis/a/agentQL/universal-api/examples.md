# AgentQL Universal API Examples

These examples use the MindCloud API key and AgentQL connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Usage

Retrieves API key usage and subscription details from AgentQL.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agentQL/latest/actions/get-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agentQL/latest/actions/get-usage?${params}`, {
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

See the full [Get Usage action reference](actions/get-usage.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/agentQL/latest/actions/get-usage).

## Create Remote Browser Session

Creates a remote browser session with CDP access in AgentQL.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/agentQL/latest/actions/create-remote-browser-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/agentQL/latest/actions/create-remote-browser-session', {
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
  "data": [],
  "meta": {}
}
```

See the full [Create Remote Browser Session action reference](actions/create-remote-browser-session.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/agentQL/latest/actions/create-remote-browser-session).
