# Agent Mail Universal API Examples

These examples use the MindCloud API key and Agent Mail connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Inboxes

Retrieves inboxes from AgentMail for the authenticated account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/list-inboxes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/list-inboxes?${params}`, {
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
      "client_id": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "display_name": "Ava Chen",
      "email": "ava@example.com",
      "inbox_id": "string",
      "pod_id": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [List Inboxes action reference](actions/list-inboxes.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/agentMail/latest/actions/list-inboxes).

## Create Inbox

Creates a new inbox in AgentMail.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/create-inbox" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/create-inbox', {
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
      "client_id": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "display_name": "Ava Chen",
      "email": "ava@example.com",
      "inbox_id": "string",
      "pod_id": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Create Inbox action reference](actions/create-inbox.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/agentMail/latest/actions/create-inbox).
