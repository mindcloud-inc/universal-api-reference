# Userflow Universal API Examples

These examples use the MindCloud API key and Userflow connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Users

Retrieves a list of users from Userflow.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/userflow/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/userflow/latest/actions/list-users?${params}`, {
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
      "data": [
        {
          "attributes": {
            "email": "ava@example.com",
            "name": "Ava Chen"
          },
          "created_at": "2026-05-07T12:00:00.000Z",
          "groups": {},
          "id": "string",
          "memberships": {},
          "object": "string"
        }
      ],
      "has_more": true,
      "next_page_url": "https://example.com",
      "object": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List Users action reference](actions/list-users.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/userflow/latest/actions/list-users).

## Create Or Update Group

Creates or updates a group in Userflow.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/userflow/latest/actions/create-or-update-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/userflow/latest/actions/create-or-update-group', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
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
      "attributes": {
        "name": "Ava Chen"
      },
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "memberships": {},
      "object": "string",
      "users": {}
    }
  ],
  "meta": {}
}
```

See the full [Create Or Update Group action reference](actions/create-or-update-group.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/userflow/latest/actions/create-or-update-group).
