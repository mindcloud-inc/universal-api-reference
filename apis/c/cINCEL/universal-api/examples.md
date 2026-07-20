# CINCEL Universal API Examples

These examples use the MindCloud API key and CINCEL connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List User Teams



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cINCEL/latest/actions/list-user-teams?connectionId=$CONNECTION_ID&limit=25&offset=0&user=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "user": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cINCEL/latest/actions/list-user-teams?${params}`, {
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
      "createdAt": "string",
      "deletedAt": {},
      "emoji": {},
      "isDefaultTeam": true,
      "logo": "string",
      "name": "Ava Chen",
      "role": "string",
      "updatedAt": "string",
      "uuid": "string",
      "workspace": {}
    }
  ],
  "meta": {}
}
```

See the full [List User Teams action reference](actions/list-user-teams.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cINCEL/latest/actions/list-user-teams).

## Create Contact



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cINCEL/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "team": "string",
  "name": "Ava Chen",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cINCEL/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "team": "string",
    "name": "Ava Chen",
    "email": "ava@example.com"
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "name": "Ava Chen",
      "team": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Contact action reference](actions/create-contact.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cINCEL/latest/actions/create-contact).
