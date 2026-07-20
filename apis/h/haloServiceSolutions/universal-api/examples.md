# Halo Service Solutions Universal API Examples

These examples use the MindCloud API key and Halo Service Solutions connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current Agent

Retrieves the current agent from Halo Service Solutions.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/get-current-agent?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/get-current-agent?${params}`, {
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

See the full [Get Current Agent action reference](actions/get-current-agent.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/haloServiceSolutions/latest/actions/get-current-agent).

## Create Action

Creates a new action in Halo Service Solutions.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/create-action" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ticket_id": 1,
  "outcome": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/create-action', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ticket_id": 1,
    "outcome": "string"
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
      "actionby_agent_id": 1,
      "actiondatecreated": "2026-05-07T12:00:00.000Z",
      "datetime": "2026-05-07T12:00:00.000Z",
      "guid": "string",
      "id": 1,
      "new_status": 1,
      "note": "string",
      "old_status": 1,
      "outcome": "string",
      "ticket_id": 1,
      "unread": 1,
      "who": "string",
      "who_agentid": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Action action reference](actions/create-action.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/haloServiceSolutions/latest/actions/create-action).
