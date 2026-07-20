# Rocketlane Universal API Examples

These examples use the MindCloud API key and Rocketlane connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Users

Lists users in Rocketlane.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rocketlane/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rocketlane/latest/actions/list-users?${params}`, {
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
      "capacityInMinutes": 1,
      "company": {},
      "createdAt": 1,
      "createdBy": {},
      "email": "ava@example.com",
      "fields": [
        {}
      ],
      "firstName": "Ava",
      "holidayCalendar": {},
      "lastName": "Chen",
      "permission": {},
      "profilePictureUrl": "https://example.com",
      "role": {},
      "status": "string",
      "type": "string",
      "updatedAt": 1,
      "updatedBy": {},
      "userId": 1
    }
  ],
  "meta": {}
}
```

See the full [List Users action reference](actions/list-users.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rocketlane/latest/actions/list-users).

## Add Conversation Members

Adds members to a conversation in Rocketlane.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rocketlane/latest/actions/add-conversation-members" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "conversationId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rocketlane/latest/actions/add-conversation-members', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "conversationId": 1
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
      "conversationId": 1,
      "members": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Add Conversation Members action reference](actions/add-conversation-members.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rocketlane/latest/actions/add-conversation-members).
