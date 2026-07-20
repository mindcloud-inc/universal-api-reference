# Bonusly Universal API Examples

These examples use the MindCloud API key and Bonusly connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Me

Retrieves the authenticated user from Bonusly.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bonusly/latest/actions/me?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bonusly/latest/actions/me?${params}`, {
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
      "displayName": "Ava Chen",
      "earningBalance": 1,
      "email": "ava@example.com",
      "givingBalance": 1,
      "id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Me action reference](actions/me.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bonusly/latest/actions/me).

## Admin Create User

Creates a new user in Bonusly.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bonusly/latest/actions/admin-create-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "firstName": "Ava",
  "lastName": "Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bonusly/latest/actions/admin-create-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "firstName": "Ava",
    "lastName": "Chen"
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
      "createdAt": "string",
      "displayName": "Ava Chen",
      "email": "ava@example.com",
      "id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Admin Create User action reference](actions/admin-create-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bonusly/latest/actions/admin-create-user).
