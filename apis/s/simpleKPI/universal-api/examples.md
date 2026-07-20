# SimpleKPI Universal API Examples

These examples use the MindCloud API key and SimpleKPI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Users

Retrieves user records from a SimpleKPI account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simpleKPI/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simpleKPI/latest/actions/list-users?${params}`, {
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
      "can_admin_settings": true,
      "can_manage_users": true,
      "created_at": "string",
      "email": "ava@example.com",
      "first_name": "Ava",
      "id": 1,
      "last_login_at": "string",
      "last_name": "Chen",
      "last_password_changed_at": "string",
      "password": "string",
      "updated_at": "string",
      "user_status_id": "string",
      "user_type": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Users action reference](actions/list-users.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/simpleKPI/latest/actions/list-users).

## Create Group

Creates a new group in SimpleKPI.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/simpleKPI/latest/actions/create-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/simpleKPI/latest/actions/create-group', {
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
      "created_at": "string",
      "id": 1,
      "name": "Ava Chen",
      "sort_order": 1,
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Group action reference](actions/create-group.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/simpleKPI/latest/actions/create-group).
