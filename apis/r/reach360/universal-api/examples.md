# Reach360 Universal API Examples

These examples use the MindCloud API key and Reach360 connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Users

Retrieves all users from Reach360.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reach360/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reach360/latest/actions/list-users?${params}`, {
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
      "articulate360User": true,
      "email": "ava@example.com",
      "favoritesUrl": "https://example.com",
      "firstName": "Ava",
      "groupsUrl": "https://example.com",
      "id": "string",
      "lastActiveAt": "2026-05-07T12:00:00.000Z",
      "lastName": "Chen",
      "learnerReportUrl": "https://example.com",
      "managingGroupsUrl": "https://example.com",
      "reportingGroupsUrl": "https://example.com",
      "role": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List Users action reference](actions/list-users.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/reach360/latest/actions/list-users).

## Add User To Group

Adds a user to a Reach360 group.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/reach360/latest/actions/add-user-to-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupId": "string",
  "userId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/reach360/latest/actions/add-user-to-group', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groupId": "string",
    "userId": "string"
  })
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

See the full [Add User To Group action reference](actions/add-user-to-group.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/reach360/latest/actions/add-user-to-group).
