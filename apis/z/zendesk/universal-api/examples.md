# Zendesk Universal API Examples

These examples use the MindCloud API key and Zendesk connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Users

Retrieves a list of users from Zendesk.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/list-users?${params}`, {
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
      "active": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "id": 1,
      "lastLoginAt": "2026-05-07T12:00:00.000Z",
      "locale": "string",
      "name": "Ava Chen",
      "organizationId": 1,
      "role": "string",
      "timeZone": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List Users action reference](actions/list-users.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zendesk/latest/actions/list-users).

## Create Group Membership

Creates a new group membership in Zendesk.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/create-group-membership" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "group_membership.user_id": 1,
  "group_membership.group_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/create-group-membership', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "group_membership.user_id": 1,
    "group_membership.group_id": 1
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
      "default": true,
      "groupId": 1,
      "id": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "userId": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Group Membership action reference](actions/create-group-membership.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zendesk/latest/actions/create-group-membership).
