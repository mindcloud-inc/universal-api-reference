# CallPage Universal API Examples

These examples use the MindCloud API key and CallPage connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Users

Retrieves all available users from CallPage.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callPage/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/callPage/latest/actions/list-users?${params}`, {
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
      "activatedAt": "string",
      "avatar": {},
      "callerId": {
        "activatedAt": {},
        "id": 1,
        "updatedAt": "string"
      },
      "email": "ava@example.com",
      "id": 1,
      "lastOnline": {},
      "name": "Ava Chen",
      "parentId": {},
      "role": {
        "slug": "string"
      },
      "tel": "string",
      "telExtension": {},
      "telFormatted": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Users action reference](actions/list-users.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/callPage/latest/actions/list-users).

## Add Users To Widget

Adds users to an existing widget in CallPage.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/callPage/latest/actions/add-users-to-widget" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "userIds": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/callPage/latest/actions/add-users-to-widget', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "userIds": 1
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
      "assignment_id": 1,
      "user_id": 1
    }
  ],
  "meta": {}
}
```

See the full [Add Users To Widget action reference](actions/add-users-to-widget.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/callPage/latest/actions/add-users-to-widget).
