# Cronly Universal API Examples

These examples use the MindCloud API key and Cronly connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Users



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cronly/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cronly/latest/actions/list-users?${params}`, {
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
      "company_id": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "id": 1,
      "is_super_admin": true,
      "name": "Ava Chen",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [List Users action reference](actions/list-users.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cronly/latest/actions/list-users).

## Create Backup



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cronly/latest/actions/create-backup" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "username": "Ava Chen",
  "serverId": "string",
  "fileContent": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cronly/latest/actions/create-backup', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "username": "Ava Chen",
    "serverId": "string",
    "fileContent": "string"
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
      "company_id": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "server_id": 1,
      "updated_at": "2026-05-07T12:00:00.000Z",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Create Backup action reference](actions/create-backup.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cronly/latest/actions/create-backup).
