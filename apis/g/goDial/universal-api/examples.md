# GoDial Universal API Examples

These examples use the MindCloud API key and GoDial connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Teams

Retrieves a list of teams from GoDial.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goDial/latest/actions/team-list?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goDial/latest/actions/team-list?${params}`, {
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
      "companyId": "string",
      "createdOn": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Teams action reference](actions/team-list.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/goDial/latest/actions/team-list).

## Create User

Creates a new user in GoDial.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/goDial/latest/actions/accounts-add" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goDial/latest/actions/accounts-add', {
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
      "email": "ava@example.com",
      "id": "string",
      "name": "Ava Chen",
      "role": "string",
      "teamsId": [
        "string"
      ],
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Create User action reference](actions/accounts-add.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/goDial/latest/actions/accounts-add).
