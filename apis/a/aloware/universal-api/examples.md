# Aloware Universal API Examples

These examples use the MindCloud API key and Aloware connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Users

Retrieves user records from your Aloware account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aloware/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aloware/latest/actions/list-users?${params}`, {
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
      "agentStatus": 1,
      "email": "ava@example.com",
      "humanReadableAgentStatus": "string",
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Users action reference](actions/list-users.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/aloware/latest/actions/list-users).

## Clear User Power Dialer Lists

Clears all contacts from an Aloware user's power dialer lists.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/aloware/latest/actions/clear-user-power-dialer-lists" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aloware/latest/actions/clear-user-power-dialer-lists', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userId": "string"
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
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Clear User Power Dialer Lists action reference](actions/clear-user-power-dialer-lists.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/aloware/latest/actions/clear-user-power-dialer-lists).
